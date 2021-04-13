---
title: Errori comuni del compilatore
description: In questa sezione vengono illustrati gli errori tipici del compilatore che si verificano durante la migrazione di una codebase esistente. Questi esempi possono provenire dal codice HAL a livello di sistema, sebbene i concetti siano direttamente applicabili al codice a livello di utente.
ms.assetid: bbb6a57f-281a-4a6e-a4b6-15846d0cf21f
keywords:
- errori del compilatore programmazione Windows a 64 bit
- migrazione della programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a84a5f5f58f2cab7555ce3401ed6fae0af240f4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104339698"
---
# <a name="common-compiler-errors"></a>Errori comuni del compilatore

In questa sezione vengono illustrati gli errori tipici del compilatore che si verificano durante la migrazione di una codebase esistente. Questi esempi possono provenire dal codice HAL a livello di sistema, sebbene i concetti siano direttamente applicabili al codice a livello di utente.

## <a name="warning-c4311-example-1"></a>Avviso C4311 esempio 1

' Type cast ': troncamento puntatore da' void \* \_ \_ ptr64' a' unsigned long

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Codice
</dt> <dd>

`pPciAddr->u.AsULONG = (ULONG) CIA_PCI_CONFIG_BASE_QVA;`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

**PtrToUlong** è una funzione inline o una macro, a seconda dell'utilizzo. Tronca un puntatore a un **ULONG**. Sebbene i puntatori a 32 bit non siano interessati, la metà superiore di un puntatore a 64 bit viene troncata.

CIA \_ PCI \_ config \_ base \_ QVA è dichiarato come **PVOID**. Il cast **ULONG** funziona nel mondo a 32 bit, ma genera un errore nel mondo a 64 bit. La soluzione consiste nell'ottenere un puntatore a 64 bit a un **ULONG**, perché la modifica della definizione dell'Unione a cui pPciAddr >u. AsULONG è definita in modifica troppa quantità di codice.

L'uso della macro **PtrToUlong** per convertire **PVOID** a 64 bit nell'oggetto **ULONG** necessario è consentito perché sono disponibili informazioni sul valore specifico di CIA \_ PCI \_ config \_ base \_ QVA. In questo caso, il puntatore non avrà mai dati nei bit 32 superiori.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluzione
</dt> <dd>

`pPciAddr->u.AsULONG = PtrToUlong(CIA_PCI_CONFIG_BASE_QVA);`

</dd> </dl>

## <a name="warning-c4311-example-2"></a>Avviso C4311 esempio 2

' Type cast ': troncamento puntatore da' struct \_ Error \_ frame \* \_ \_ ptr64' a' unsigned long

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Codice
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG)PUncorrectableError );`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

Il problema è che l'ultimo parametro di questa funzione è un puntatore a una struttura di dati. Poiché PUncorrectableError è un puntatore, viene modificata la dimensione con il modello di programmazione. Il prototipo per **KeBugCheckEx** è stato modificato in modo che l'ultimo parametro sia un **\_ ptr ULONG**. Di conseguenza, è necessario eseguire il cast del puntatore a funzione a un **\_ ptr ULONG**.

È possibile chiedersi perché **PVOID** non è stato usato come ultimo parametro. A seconda del contesto della chiamata, l'ultimo parametro può essere diverso da un puntatore o forse da un codice di errore.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluzione
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG_PTR)PUncorrectableError );`

</dd> </dl>

## <a name="warning-c4244-example-1"></a>Avviso C4244 esempio 1

' =': conversione da' struct \_ Configuration \_ Component \* \_ \_ ptr64' a' struct \_ Configuration \_ Component \* ', possibile perdita di dati

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Codice
</dt> <dd>

`Component = &CurrentEntry->ComponentEntry;`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

La funzione dichiara il componente della variabile come componente PCONFIGURATION \_ . Successivamente, la variabile viene utilizzata nell'assegnazione seguente che risulta corretta:

`Component = &CurrentEntry->ComponentEntry;`

Il componente PCONFIGURATION del tipo \_ viene tuttavia definito come segue:

``` syntax
typedef struct __CONFIGURATION_COMPONENT {
...
...
} CONFIGURATION_COMPONENT, * POINTER_32 PCONFIGURATION_COMPONENT;
```

La definizione del tipo per il \_ componente PCONFIGURATION fornisce un puntatore a 32 bit sia nei modelli a 32 bit che in quelli a 64 bit, perché è dichiarato **puntatore \_ 32**. La finestra di progettazione originale di questa struttura sapeva che era destinata a essere usata in un contesto a 32 bit nel BIOS ed è stata definita espressamente per tale uso. Questo codice funziona correttamente in Windows a 32 bit perché i puntatori sono a 32 bit. In Windows a 64 bit non funziona perché il codice è nel contesto a 64 bit.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluzione
</dt> <dd>

Per risolvere questo problema, usare \_ \* il componente di configurazione anziché il componente PCONFIGURATION a 32 bit \_ . È importante comprendere chiaramente lo scopo del codice. Se il codice ha lo scopo di toccare il BIOS a 32 bit o lo spazio del sistema, la correzione non funzionerà.

Il **puntatore \_ 32** è definito in Ntdef. h e Winnt. h.

``` syntax
#ifdef (__AXP64__)
#define POINTER_32 _ptr32
#else
#define POINTER_32
#endif
```

</dd> </dl>

## <a name="warning-c4242-example-2"></a>Avviso C4242 esempio 2

' =': conversione da' \_ \_ Int64' a' unsigned long ', possibile perdita di dati

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Codice
</dt> <dd>

``` syntax
ARC_STATUS HalpCopyNVRamBuffer (
IN PCHAR NvDestPtr,
IN PCHAR NvSrcPtr,
IN ULONG Length )
{

ULONG PageSelect1, ByteSelect1;

ByteSelect1 = (NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;

ByteSelect1 = (NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

Questo avviso viene generato perché il calcolo utilizza valori a 64 bit, in questo caso puntatori e inserendo il risultato in un **ULONG** a 32 bit.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluzione
</dt> <dd>

Digitare il risultato del calcolo in un **ULONG** come illustrato di seguito:

`ByteSelect1 = (ULONG)(NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;`

Typecasting il risultato consente al compilatore di sapere se il risultato è certo. Detto questo, assicurarsi di avere compreso il calcolo e di essere in grado di rientrare in un **ULONG** a 32 bit.

Se il risultato potrebbe non rientrare in un **ULONG** a 32 bit, modificare il tipo di base della variabile che conterrà il risultato.

</dd> </dl>

## <a name="warning-c4311---example-1"></a>Avviso C4311-esempio 1

' Type cast ': troncamento puntatore da' void \* \_ \_ ptr64' a' unsigned long '

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Codice
</dt> <dd>

``` syntax
ULONG HalpMapDebugPort(
IN ULONG ComPort,
OUT PULONG ReadQva,
OUT PULONG WriteQva)
{
ULONG ComPortAddress;

ULONG PortQva;

// Compute the port address, based on the desired com port.

switch( ComPort ){
case 1:
   ComPortAddress = COM1_ISA_PORT_ADDRESS;
   break;

case 2:
default:
   ComPortAddress = COM2_ISA_PORT_ADDRESS;
}
PortQva = (ULONG)HAL_MAKE_QVA(CIA_PCI_SPARSE_IO_PHYSICAL) + ComPortAddress;

// Return the QVAs for read and write access.

*ReadQva = PortQva;
*WriteQva = PortQva;

return ComPortAddress;
}
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

Questa funzione completa gestisce gli indirizzi come numeri interi, rendendo necessaria la necessità di digitare tali numeri interi in modo portatile. Tutte le variabili locali, i valori intermedi nei calcoli e i valori restituiti devono essere tipi portabili.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluzione
</dt> <dd>

``` syntax
ULONG_PTR HalpMapDebugPort(
IN ULONG ComPort,
OUT PULONG_PTR ReadQva,
OUT PULONG_PTR WriteQva)
{
ULONG_PTR ComPortAddress;

ULONG_PTR PortQva;

// Compute the port address, based on the desired com port.

switch( ComPort ){
case 1:
   ComPortAddress = COM1_ISA_PORT_ADDRESS;
   break;

case 2:
default:
   ComPortAddress = COM2_ISA_PORT_ADDRESS;
}

PortQva = (ULONG_PTR)HAL_MAKE_QVA(CIA_PCI_SPARSE_IO_PHYSICAL) + ComPortAddress;

// Return the QVAs for read and write access.

*ReadQva = PortQva;
*WriteQva = PortQva;

return ComPortAddress;
}
```

**PULONG \_ PTR** è un puntatore che si trova a 32 bit per Windows a 32 bit e 64 bit per Windows a 64 bit. Punta a un Unsigned Integer, **ULONG \_ ptr**, che è 32 bit per Windows a 32 bit e 64 bit per Windows a 64 bit.

</dd> </dl>

## <a name="warning-c4311---example-2"></a>Avviso C4311-esempio 2

' Type cast ': troncamento puntatore da' void \* \_ \_ ptr64' a' unsigned long '

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Codice
</dt> <dd>

``` syntax
BOOLEAN
HalpMapIoSpace (
VOID
)
{
PVOID PciIoSpaceBase;
PciIoSpaceBase = HAL_MAKE_QVA( CIA_PCI_SPARSE_IO_PHYSICAL );

//Map base addresses in QVA space.

HalpCMOSRamBase = (PVOID)((ULONG)PciIoSpaceBase + CMOS_ISA_PORT_ADDRESS);
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

Anche se tutti i valori di QVA (quasi Virtual Address) sono effettivamente valori a 32 bit in questa fase e si adattano a un **ULONG**, è più coerente considerare tutti gli indirizzi come valori **\_ ptr ULONG** , quando possibile.

Il puntatore PciIoSpaceBase include il QVA creato nella macro HAL \_ make \_ QVA. Questa macro restituisce un valore a 64 bit con i primi 32 bit impostati su zero, in modo che la matematica funzionerà. È possibile lasciare semplicemente il codice per troncare il puntatore in un **ULONG**, ma questa pratica è sconsigliata per migliorare la gestibilità e la portabilità del codice. Ad esempio, il contenuto di un QVA potrebbe cambiare in futuro per usare alcuni dei bit superiori a questo livello, suddividendo il codice.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluzione
</dt> <dd>

Essere sicuri e usare **il \_ ptr ULONG** per tutti gli indirizzi e i calcoli matematici.

`HalpCMOSRamBase = (PVOID)((ULONG_PTR)PciIoSpaceBase + CMOS_ISA_PORT_ADDRESS);`

</dd> </dl>

## <a name="warning-c4311-example-3"></a>Esempio di C4311 di avviso 3

' Type cast ': troncamento puntatore da' void \* \_ \_ ptr64' a' unsigned long '

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Codice
</dt> <dd>

``` syntax
PVOID
HalDereferenceQva(
PVOID Qva,
INTERFACE_TYPE InterfaceType,
ULONG BusNumber)

if ( ((ULONG) Qva & QVA_SELECTORS) == QVA_ENABLE ) {

return( (PVOID)( (ULONG)Qva << IO_BIT_SHIFT ) );
} 
else {
return (Qva);
}
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

Il compilatore genera un avviso sull'indirizzo degli operatori (&) e di spostamento a sinistra (<<) se vengono applicati ai tipi di puntatore. Nel codice precedente, QVA è un valore **PVOID** . È necessario eseguirne il cast a un tipo integer per eseguire la matematica. Poiché il codice deve essere portabile, utilizzare **ULONG \_ ptr** anziché **ULONG**.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluzione
</dt> <dd>

``` syntax
if ( ((ULONG_PTR) Qva & QVA_SELECTORS) == QVA_ENABLE ) {
  return( (PVOID)( (ULONG_PTR)Qva << IO_BIT_SHIFT ) );
```

</dd> </dl>

## <a name="warning-c4311-example-4"></a>Avviso C4311 esempio 4

' Type cast ': troncamento puntatore da' void \* \_ \_ ptr64' a' unsigned long '

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Codice
</dt> <dd>

``` syntax
TranslatedAddress->LowPart = (ULONG)HalCreateQva(
*TranslatedAddress, va);
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

TranslatedAddress è un'Unione che ha un aspetto simile al seguente:

``` syntax
typedef union
   Struct {
      ULONG LowPart;
      LONG Highpart;
   }
   LONGLONG QuadPart;
}
```

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluzione
</dt> <dd>

Conoscendo il resto del codice potrebbe essere inserito in HighPart, è possibile selezionare una delle soluzioni illustrate qui.

`TranslatedAddress->LowPart = PtrToUlong(HalCreateQva(*TranslatedAddress,va) );`

La macro **PtrToUlong** tronca il puntatore restituito da **HalCreateQva** a 32 bit. Sappiamo che QVA restituito da **HalCreateQva** ha i bit 32 superiori impostati su zero e la riga di codice successiva imposta TranslatedAddress->HighPart su zero.

Con cautela, è possibile usare gli elementi seguenti:

`TranslatedAddress->QuadPart = (LONGLONG)HalCreateQva(*TranslatedAddress,va);`

Questa operazione funziona in questo esempio: la macro **HalCreateQva** restituisce 64 bit, con i bit 32 superiore impostati su zero. È sufficiente evitare di lasciare invariati i 32 bit superiori in un ambiente a 32 bit, che la seconda soluzione può effettivamente eseguire.

</dd> </dl>

## <a name="warning-c4311-example-5"></a>Avviso C4311 esempio 5

' Type cast ': troncamento puntatore da' void \* \_ \_ ptr64' a' unsigned long '

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Codice
</dt> <dd>

``` syntax
VOID
HalpCiaProgramDmaWindow(
PWINDOW_CONTROL_REGISTERS WindowRegisters,
PVOID MapRegisterBase
)
{
CIA_WBASE Wbase;

Wbase.all = 0;
Wbase.Wen = 1;
Wbase.SgEn = 1;
Wbase.Wbase = (ULONG)(WindowRegisters->WindowBase) >> 20;
```

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

WindowRegisters->WindowBase è un puntatore e ora è 64 bit. Il codice dice di spostare a destra questo valore di 20 bit. Il compilatore non consentirà di usare l'operatore di spostamento a destra (>>) su un puntatore. Pertanto, è necessario eseguirne il cast a un tipo Integer.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluzione
</dt> <dd>

`Wbase.Wbase= PtrToUlong ( (PVOID) ((ULONG_PTR) (WindowRegisters->WindowBase) >> 20));`

Il cast a **un \_ ptr ULONG** è solo quello che serve. Il problema successivo è wbase. Wbase è un **ULONG** e è 32 bit. In questo caso, è noto che il puntatore a 64 bit WindowRegisters->WindowBase è valido nei 32 bit inferiori anche dopo essere stato spostato. In questo modo si usa la macro **PtrToUlong** accettabile, perché tronca il puntatore a 64 bit in un **ULONG** a 32 bit. Il cast **PVOID** è necessario perché **PtrToUlong** prevede un argomento puntatore. Quando si esamina il codice assembler risultante, tutto questo cast del codice C diventa solo un quad di carico, uno spostamento a destra e un archivio lungo.

</dd> </dl>

 

 




