---
title: Errori comuni del compilatore
description: Questa sezione illustra gli errori tipici del compilatore che si verificano durante la migrazione di una codebase esistente. Questi esempi derivano da codice HAL a livello di sistema, anche se i concetti sono direttamente applicabili al codice a livello di utente.
ms.assetid: bbb6a57f-281a-4a6e-a4b6-15846d0cf21f
keywords:
- Errori del compilatore a 64 bit Windows programmazione
- migrazione a 64 bit Windows programmazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55d12e7c5566b5cb2b934eefb71b1b51858f278d3e408d3080cb1810f185dcfb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071641"
---
# <a name="common-compiler-errors"></a>Errori comuni del compilatore

Questa sezione illustra gli errori tipici del compilatore che si verificano durante la migrazione di una codebase esistente. Questi esempi derivano da codice HAL a livello di sistema, anche se i concetti sono direttamente applicabili al codice a livello di utente.

## <a name="warning-c4311-example-1"></a>Avviso C4311 Esempio 1

'type cast': troncamento del puntatore da 'void \* \_ \_ ptr64' a 'unsigned long'

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Codice
</dt> <dd>

`pPciAddr->u.AsULONG = (ULONG) CIA_PCI_CONFIG_BASE_QVA;`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

**PtrToUlong** è una funzione o una macro inline, a seconda dell'utilizzo. Tronca un puntatore a un **ULONG**. Anche se i puntatori a 32 bit non sono interessati, la metà superiore di un puntatore a 64 bit viene troncata.

CIA \_ PCI \_ CONFIG BASE \_ \_ QVA è dichiarato come **PVOID**. Il cast **ULONG** funziona nel mondo a 32 bit, ma comporta un errore nel mondo a 64 bit. La soluzione consiste nel ottenere un puntatore a 64 bit a **ULONG**, perché modificando la definizione dell'unione che pPciAddr->u.AsULONG è definito nelle modifiche troppo codice.

L'uso della macro **PtrToUlong** per convertire **il valore PVOID** a 64 bit nell'ULONG necessario è consentito perché si ha conoscenza del valore specifico di CIA  \_ PCI CONFIG BASE \_ \_ \_ QVA. In questo caso, questo puntatore non avrà mai dati nei 32 bit superiori.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluzione
</dt> <dd>

`pPciAddr->u.AsULONG = PtrToUlong(CIA_PCI_CONFIG_BASE_QVA);`

</dd> </dl>

## <a name="warning-c4311-example-2"></a>Avviso C4311 Esempio 2

'type cast': troncamento del puntatore da 'struct \_ ERROR \_ FRAME \* \_ \_ ptr64' a 'unsigned long

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Codice
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG)PUncorrectableError );`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

Il problema è che l'ultimo parametro di questa funzione è un puntatore a una struttura di dati. Poiché PUncorrectableError è un puntatore, cambia le dimensioni con il modello di programmazione. Il prototipo **per KeBugCheckEx** è stato modificato in modo che l'ultimo parametro sia **un ULONG \_ PTR**. Di conseguenza, è necessario eseguire il cast del puntatore a funzione a **un ULONG \_ PTR.**

Si potrebbe chiedere perché **PVOID** non è stato usato come ultimo parametro. A seconda del contesto della chiamata, l'ultimo parametro può essere diverso da un puntatore o forse da un codice di errore.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluzione
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG_PTR)PUncorrectableError );`

</dd> </dl>

## <a name="warning-c4244-example-1"></a>Avviso C4244 Esempio 1

'=': conversione da 'struct \_ CONFIGURATION \_ COMPONENT \* \_ \_ ptr64 ' a 'struct CONFIGURATION \_ \_ \* COMPONENT', possibile perdita di dati

<dl> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Codice
</dt> <dd>

`Component = &CurrentEntry->ComponentEntry;`

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

La funzione dichiara la variabile Component come PCONFIGURATION \_ COMPONENT. Successivamente, la variabile viene usata nell'assegnazione seguente che appare corretta:

`Component = &CurrentEntry->ComponentEntry;`

Tuttavia, il tipo PCONFIGURATION \_ COMPONENT è definito come:

``` syntax
typedef struct __CONFIGURATION_COMPONENT {
...
...
} CONFIGURATION_COMPONENT, * POINTER_32 PCONFIGURATION_COMPONENT;
```

La definizione del tipo per PCONFIGURATION COMPONENT fornisce un puntatore a 32 bit in entrambi i modelli a 32 bit e a 64 bit perché è \_ dichiarato **POINTER \_ 32**. La finestra di progettazione originale di questa struttura era in grado di usarla in un contesto a 32 bit nel BIOS ed è stata espressamente definita per tale utilizzo. Questo codice funziona correttamente in Windows a 32 bit perché i puntatori sono a 32 bit. Nelle applicazioni a 64 bit Windows non funziona perché il codice si trova nel contesto a 64 bit.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluzione
</dt> <dd>

Per risolvere questo problema, usare CONFIGURATION COMPONENT anziché PCONFIGURATION COMPONENT a \_ \* 32 \_ bit. È importante comprendere chiaramente lo scopo del codice. Se questo codice è destinato a toccare il BIOS a 32 bit o lo spazio di sistema, questa correzione non funzionerà.

**POINTER \_ 32** è definito in Ntdef.h e Winnt.h.

``` syntax
#ifdef (__AXP64__)
#define POINTER_32 _ptr32
#else
#define POINTER_32
#endif
```

</dd> </dl>

## <a name="warning-c4242-example-2"></a>Avviso C4242 Esempio 2

'=': conversione da ' \_ \_ int64 ' a 'unsigned long', possibile perdita di dati

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

Questo avviso viene generato perché il calcolo usa valori a 64 bit, in questo caso puntatori, e inserisce il risultato in un **ULONG** a 32 bit.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluzione
</dt> <dd>

Il tipo esegue il cast del risultato del calcolo a **un ULONG,** come illustrato di seguito:

`ByteSelect1 = (ULONG)(NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;`

Il typecasting del risultato indica al compilatore di essere certi del risultato. Detto questo, assicurarsi di aver compreso il calcolo e di essere certi che si adatterà a un **ULONG** a 32 bit.

Se il risultato potrebbe non rientrare in un **ULONG** a 32 bit, modificare il tipo di base della variabile che contenerà il risultato.

</dd> </dl>

## <a name="warning-c4311---example-1"></a>Avviso C4311 - Esempio 1

'type cast': troncamento del puntatore da 'void \* \_ \_ ptr64' a 'unsigned long'

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

Questa intera funzione gestisce gli indirizzi come numeri interi, richiedendo la necessità di digitare tali numeri interi in modo portabile. Tutte le variabili locali, i valori intermedi nei calcoli e i valori restituiti devono essere tipi portabili.

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

**PULONG \_ PTR** è un puntatore a 32 bit per i Windows a 32 bit e a 64 bit per i Windows a 64 bit. Punta a un intero senza segno, **ULONG \_ PTR,** che è a 32 bit per i Windows a 32 bit e a 64 bit per i Windows.

</dd> </dl>

## <a name="warning-c4311---example-2"></a>Avviso C4311 - Esempio 2

'type cast': troncamento del puntatore da 'void \* \_ \_ ptr64' a 'unsigned long'

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

Anche se tutti i valori QVA (Quasi Virtual Address) sono in realtà valori a 32 bit in questa fase e rientrano in **un ULONG,** è più coerente considerare tutti gli indirizzi come valori **\_ ULONG PTR,** se possibile.

Il puntatore PciIoSpaceBase contiene l'QVA creata nella macro HAL \_ MAKE \_ QVA. Questa macro restituisce un valore a 64 bit con i primi 32 bit impostati su zero in modo che i calcoli matematici funzionino. È possibile lasciare semplicemente il codice per troncare il puntatore in **un ULONG,** ma questa procedura è sconsigliata per migliorare la manutenibilità e la portabilità del codice. Ad esempio, il contenuto di una QVA potrebbe cambiare in futuro per usare alcuni dei bit superiori a questo livello, causando un'interruzione del codice.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluzione
</dt> <dd>

Essere sicuri e usare **ULONG \_ PTR per tutti** gli indirizzi e i puntatori matematici.

`HalpCMOSRamBase = (PVOID)((ULONG_PTR)PciIoSpaceBase + CMOS_ISA_PORT_ADDRESS);`

</dd> </dl>

## <a name="warning-c4311-example-3"></a>Avviso C4311 Esempio 3

'type cast': troncamento del puntatore da 'void \* \_ \_ ptr64' a 'unsigned long'

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

Il compilatore avvisa dell'indirizzo degli operatori (&) e di spostamento a sinistra (<<) se vengono applicati ai tipi puntatore. Nel codice precedente, Qva è un **valore PVOID.** È necessario eseguire il cast di tale oggetto a un tipo integer per eseguire i calcoli matematici. Poiché il codice deve essere portabile, usare **ULONG \_ PTR** anziché **ULONG**.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluzione
</dt> <dd>

``` syntax
if ( ((ULONG_PTR) Qva & QVA_SELECTORS) == QVA_ENABLE ) {
  return( (PVOID)( (ULONG_PTR)Qva << IO_BIT_SHIFT ) );
```

</dd> </dl>

## <a name="warning-c4311-example-4"></a>Avviso C4311 Esempio 4

'type cast': troncamento del puntatore da 'void \* \_ \_ ptr64' a 'unsigned long'

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

TranslatedAddress è un'unione simile alla seguente:

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

Conoscendo il resto del codice che potrebbe essere presente in Highpart, è possibile selezionare una delle soluzioni illustrate di seguito.

`TranslatedAddress->LowPart = PtrToUlong(HalCreateQva(*TranslatedAddress,va) );`

La macro **PtrToUlong** tronca il puntatore restituito da **HalCreateQva** a 32 bit. È importante sapere che la QVA restituita da **HalCreateQva** ha i 32 bit superiori impostati su zero e che la riga di codice successiva imposta TranslatedAddress->Highpart su zero.

Con cautela, è possibile usare quanto segue:

`TranslatedAddress->QuadPart = (LONGLONG)HalCreateQva(*TranslatedAddress,va);`

Questa operazione funziona in questo esempio: la macro **HalCreateQva** restituisce 64 bit, con i 32 bit superiori impostati su zero. Prestare attenzione a non lasciare i 32 bit superiori indefiniti in un ambiente a 32 bit, operazione che questa seconda soluzione potrebbe effettivamente eseguire.

</dd> </dl>

## <a name="warning-c4311-example-5"></a>Avviso C4311 Esempio 5

'type cast': troncamento del puntatore da 'void \* \_ \_ ptr64 ' a 'unsigned long'

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

WindowRegisters->WindowBase è un puntatore ed è ora a 64 bit. Il codice indica di spostare a destra questo valore di 20 bit. Il compilatore non consente di usare l'operatore di spostamento a destra (>>) su un puntatore; Pertanto, è necessario eseguire il cast a un tipo di integer.

</dd> <dt>

<span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluzione
</dt> <dd>

`Wbase.Wbase= PtrToUlong ( (PVOID) ((ULONG_PTR) (WindowRegisters->WindowBase) >> 20));`

Il cast a **un \_ PTR ULONG** è proprio quello che serve. Il problema successivo è Wbase. Wbase è **un ULONG** ed è a 32 bit. In questo caso, si sa che il puntatore a 64 bit WindowRegisters->WindowBase è valido nei 32 bit inferiori anche dopo lo spostamento. Ciò rende accettabile l'uso della macro **PtrToUlong,** perché tronca il puntatore a 64 bit in un **ULONG** a 32 bit. Il cast **PVOID** è necessario perché **PtrToUlong** prevede un argomento puntatore. Quando si osserva il codice dell'assembler risultante, tutto questo cast di codice C diventa solo un quad di caricamento, si sposta a destra e archivia long.

</dd> </dl>

 

 




