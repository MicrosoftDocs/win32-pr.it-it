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
# <a name="common-compiler-errors"></a><span data-ttu-id="415b2-106">Errori comuni del compilatore</span><span class="sxs-lookup"><span data-stu-id="415b2-106">Common Compiler Errors</span></span>

<span data-ttu-id="415b2-107">In questa sezione vengono illustrati gli errori tipici del compilatore che si verificano durante la migrazione di una codebase esistente.</span><span class="sxs-lookup"><span data-stu-id="415b2-107">This section illustrates the typical compiler errors that occur when migrating an existing code base.</span></span> <span data-ttu-id="415b2-108">Questi esempi possono provenire dal codice HAL a livello di sistema, sebbene i concetti siano direttamente applicabili al codice a livello di utente.</span><span class="sxs-lookup"><span data-stu-id="415b2-108">These examples happen to be from system-level HAL code, although the concepts are directly applicable to user-level code.</span></span>

## <a name="warning-c4311-example-1"></a><span data-ttu-id="415b2-109">Avviso C4311 esempio 1</span><span class="sxs-lookup"><span data-stu-id="415b2-109">Warning C4311 Example 1</span></span>

<span data-ttu-id="415b2-110">' Type cast ': troncamento puntatore da' void \* \_ \_ ptr64' a' unsigned long</span><span class="sxs-lookup"><span data-stu-id="415b2-110">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long</span></span>

<dl> <dt>

<span data-ttu-id="415b2-111"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Codice</span><span class="sxs-lookup"><span data-stu-id="415b2-111"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

`pPciAddr->u.AsULONG = (ULONG) CIA_PCI_CONFIG_BASE_QVA;`

</dd> <dt>

<span data-ttu-id="415b2-112"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione</span><span class="sxs-lookup"><span data-stu-id="415b2-112"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="415b2-113">**PtrToUlong** è una funzione inline o una macro, a seconda dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="415b2-113">**PtrToUlong** is an inline function or macro, depending on your usage.</span></span> <span data-ttu-id="415b2-114">Tronca un puntatore a un **ULONG**.</span><span class="sxs-lookup"><span data-stu-id="415b2-114">It truncates a pointer to a **ULONG**.</span></span> <span data-ttu-id="415b2-115">Sebbene i puntatori a 32 bit non siano interessati, la metà superiore di un puntatore a 64 bit viene troncata.</span><span class="sxs-lookup"><span data-stu-id="415b2-115">Although 32-bit pointers are not affected, the upper half of a 64-bit pointer is truncated.</span></span>

<span data-ttu-id="415b2-116">CIA \_ PCI \_ config \_ base \_ QVA è dichiarato come **PVOID**.</span><span class="sxs-lookup"><span data-stu-id="415b2-116">CIA\_PCI\_CONFIG\_BASE\_QVA is declared as a **PVOID**.</span></span> <span data-ttu-id="415b2-117">Il cast **ULONG** funziona nel mondo a 32 bit, ma genera un errore nel mondo a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="415b2-117">The **ULONG** cast works in the 32-bit world, but results in an error in the 64-bit world.</span></span> <span data-ttu-id="415b2-118">La soluzione consiste nell'ottenere un puntatore a 64 bit a un **ULONG**, perché la modifica della definizione dell'Unione a cui pPciAddr >u. AsULONG è definita in modifica troppa quantità di codice.</span><span class="sxs-lookup"><span data-stu-id="415b2-118">The solution is to get a 64-bit pointer to a **ULONG**, because changing the definition of the union that pPciAddr->u.AsULONG is defined in changes too much code.</span></span>

<span data-ttu-id="415b2-119">L'uso della macro **PtrToUlong** per convertire **PVOID** a 64 bit nell'oggetto **ULONG** necessario è consentito perché sono disponibili informazioni sul valore specifico di CIA \_ PCI \_ config \_ base \_ QVA.</span><span class="sxs-lookup"><span data-stu-id="415b2-119">Using the macro **PtrToUlong** to convert the 64-bit **PVOID** to the needed **ULONG** is allowed because we have knowledge about the specific value of CIA\_PCI\_CONFIG\_BASE\_QVA.</span></span> <span data-ttu-id="415b2-120">In questo caso, il puntatore non avrà mai dati nei bit 32 superiori.</span><span class="sxs-lookup"><span data-stu-id="415b2-120">In this case, this pointer will never have data in the upper 32 bits.</span></span>

</dd> <dt>

<span data-ttu-id="415b2-121"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluzione</span><span class="sxs-lookup"><span data-stu-id="415b2-121"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

`pPciAddr->u.AsULONG = PtrToUlong(CIA_PCI_CONFIG_BASE_QVA);`

</dd> </dl>

## <a name="warning-c4311-example-2"></a><span data-ttu-id="415b2-122">Avviso C4311 esempio 2</span><span class="sxs-lookup"><span data-stu-id="415b2-122">Warning C4311 Example 2</span></span>

<span data-ttu-id="415b2-123">' Type cast ': troncamento puntatore da' struct \_ Error \_ frame \* \_ \_ ptr64' a' unsigned long</span><span class="sxs-lookup"><span data-stu-id="415b2-123">'type cast' : pointer truncation from 'struct \_ERROR\_FRAME \*\_\_ptr64 ' to 'unsigned long</span></span>

<dl> <dt>

<span data-ttu-id="415b2-124"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Codice</span><span class="sxs-lookup"><span data-stu-id="415b2-124"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG)PUncorrectableError );`

</dd> <dt>

<span data-ttu-id="415b2-125"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione</span><span class="sxs-lookup"><span data-stu-id="415b2-125"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="415b2-126">Il problema è che l'ultimo parametro di questa funzione è un puntatore a una struttura di dati.</span><span class="sxs-lookup"><span data-stu-id="415b2-126">The problem is that the last parameter to this function is a pointer to a data structure.</span></span> <span data-ttu-id="415b2-127">Poiché PUncorrectableError è un puntatore, viene modificata la dimensione con il modello di programmazione.</span><span class="sxs-lookup"><span data-stu-id="415b2-127">Because PUncorrectableError is a pointer, it changes size with the programming model.</span></span> <span data-ttu-id="415b2-128">Il prototipo per **KeBugCheckEx** è stato modificato in modo che l'ultimo parametro sia un **\_ ptr ULONG**.</span><span class="sxs-lookup"><span data-stu-id="415b2-128">The prototype for **KeBugCheckEx** was changed so that the last parameter is a **ULONG\_PTR**.</span></span> <span data-ttu-id="415b2-129">Di conseguenza, è necessario eseguire il cast del puntatore a funzione a un **\_ ptr ULONG**.</span><span class="sxs-lookup"><span data-stu-id="415b2-129">As a result, it's necessary to cast the function pointer to a **ULONG\_PTR**.</span></span>

<span data-ttu-id="415b2-130">È possibile chiedersi perché **PVOID** non è stato usato come ultimo parametro.</span><span class="sxs-lookup"><span data-stu-id="415b2-130">You might ask why **PVOID** was not used as the last parameter.</span></span> <span data-ttu-id="415b2-131">A seconda del contesto della chiamata, l'ultimo parametro può essere diverso da un puntatore o forse da un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="415b2-131">Depending on the context of the call, the last parameter may be something other than a pointer or perhaps an error code.</span></span>

</dd> <dt>

<span data-ttu-id="415b2-132"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluzione</span><span class="sxs-lookup"><span data-stu-id="415b2-132"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG_PTR)PUncorrectableError );`

</dd> </dl>

## <a name="warning-c4244-example-1"></a><span data-ttu-id="415b2-133">Avviso C4244 esempio 1</span><span class="sxs-lookup"><span data-stu-id="415b2-133">Warning C4244 Example 1</span></span>

<span data-ttu-id="415b2-134">' =': conversione da' struct \_ Configuration \_ Component \* \_ \_ ptr64' a' struct \_ Configuration \_ Component \* ', possibile perdita di dati</span><span class="sxs-lookup"><span data-stu-id="415b2-134">'=' : conversion from 'struct \_CONFIGURATION\_COMPONENT \*\_\_ptr64 ' to 'struct \_CONFIGURATION\_COMPONENT \*', possible loss of data</span></span>

<dl> <dt>

<span data-ttu-id="415b2-135"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Codice</span><span class="sxs-lookup"><span data-stu-id="415b2-135"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

`Component = &CurrentEntry->ComponentEntry;`

</dd> <dt>

<span data-ttu-id="415b2-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione</span><span class="sxs-lookup"><span data-stu-id="415b2-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="415b2-137">La funzione dichiara il componente della variabile come componente PCONFIGURATION \_ .</span><span class="sxs-lookup"><span data-stu-id="415b2-137">The function declares the variable Component as a PCONFIGURATION\_COMPONENT.</span></span> <span data-ttu-id="415b2-138">Successivamente, la variabile viene utilizzata nell'assegnazione seguente che risulta corretta:</span><span class="sxs-lookup"><span data-stu-id="415b2-138">Later, the variable is used in the following assignment that appears correct:</span></span>

`Component = &CurrentEntry->ComponentEntry;`

<span data-ttu-id="415b2-139">Il componente PCONFIGURATION del tipo \_ viene tuttavia definito come segue:</span><span class="sxs-lookup"><span data-stu-id="415b2-139">However, the type PCONFIGURATION\_COMPONENT is defined as:</span></span>

``` syntax
typedef struct __CONFIGURATION_COMPONENT {
...
...
} CONFIGURATION_COMPONENT, * POINTER_32 PCONFIGURATION_COMPONENT;
```

<span data-ttu-id="415b2-140">La definizione del tipo per il \_ componente PCONFIGURATION fornisce un puntatore a 32 bit sia nei modelli a 32 bit che in quelli a 64 bit, perché è dichiarato **puntatore \_ 32**.</span><span class="sxs-lookup"><span data-stu-id="415b2-140">The type definition for PCONFIGURATION\_COMPONENT provides a 32-bit pointer in both 32-bit and 64-bit models because it is declared **POINTER\_32**.</span></span> <span data-ttu-id="415b2-141">La finestra di progettazione originale di questa struttura sapeva che era destinata a essere usata in un contesto a 32 bit nel BIOS ed è stata definita espressamente per tale uso.</span><span class="sxs-lookup"><span data-stu-id="415b2-141">The original designer of this structure knew it was going to be used in a 32-bit context in the BIOS and expressly defined it for that use.</span></span> <span data-ttu-id="415b2-142">Questo codice funziona correttamente in Windows a 32 bit perché i puntatori sono a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="415b2-142">This code works fine in 32-bit Windows because the pointers happen to be 32-bit.</span></span> <span data-ttu-id="415b2-143">In Windows a 64 bit non funziona perché il codice è nel contesto a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="415b2-143">In 64-bit Windows, it does not work because the code is in 64-bit context.</span></span>

</dd> <dt>

<span data-ttu-id="415b2-144"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluzione</span><span class="sxs-lookup"><span data-stu-id="415b2-144"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="415b2-145">Per risolvere questo problema, usare \_ \* il componente di configurazione anziché il componente PCONFIGURATION a 32 bit \_ .</span><span class="sxs-lookup"><span data-stu-id="415b2-145">To work around this problem, use CONFIGURATION\_COMPONENT \* rather than the 32-bit PCONFIGURATION\_COMPONENT .</span></span> <span data-ttu-id="415b2-146">È importante comprendere chiaramente lo scopo del codice.</span><span class="sxs-lookup"><span data-stu-id="415b2-146">It is important to clearly understand the purpose of the code.</span></span> <span data-ttu-id="415b2-147">Se il codice ha lo scopo di toccare il BIOS a 32 bit o lo spazio del sistema, la correzione non funzionerà.</span><span class="sxs-lookup"><span data-stu-id="415b2-147">If this code is intended to touch 32-bit BIOS or System space, this fix will not work.</span></span>

<span data-ttu-id="415b2-148">Il **puntatore \_ 32** è definito in Ntdef. h e Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="415b2-148">**POINTER\_32** is defined in Ntdef.h and Winnt.h.</span></span>

``` syntax
#ifdef (__AXP64__)
#define POINTER_32 _ptr32
#else
#define POINTER_32
#endif
```

</dd> </dl>

## <a name="warning-c4242-example-2"></a><span data-ttu-id="415b2-149">Avviso C4242 esempio 2</span><span class="sxs-lookup"><span data-stu-id="415b2-149">Warning C4242 Example 2</span></span>

<span data-ttu-id="415b2-150">' =': conversione da' \_ \_ Int64' a' unsigned long ', possibile perdita di dati</span><span class="sxs-lookup"><span data-stu-id="415b2-150">'=' : conversion from '\_\_int64 ' to 'unsigned long ', possible loss of data</span></span>

<dl> <dt>

<span data-ttu-id="415b2-151"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Codice</span><span class="sxs-lookup"><span data-stu-id="415b2-151"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
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

<span data-ttu-id="415b2-152"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione</span><span class="sxs-lookup"><span data-stu-id="415b2-152"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="415b2-153">Questo avviso viene generato perché il calcolo utilizza valori a 64 bit, in questo caso puntatori e inserendo il risultato in un **ULONG** a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="415b2-153">This warning is generated because the calculation is using 64-bit values, in this case pointers, and placing the result in a 32-bit **ULONG**.</span></span>

</dd> <dt>

<span data-ttu-id="415b2-154"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluzione</span><span class="sxs-lookup"><span data-stu-id="415b2-154"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="415b2-155">Digitare il risultato del calcolo in un **ULONG** come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="415b2-155">Type cast the result of the calculation to a **ULONG** as shown here:</span></span>

`ByteSelect1 = (ULONG)(NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;`

<span data-ttu-id="415b2-156">Typecasting il risultato consente al compilatore di sapere se il risultato è certo.</span><span class="sxs-lookup"><span data-stu-id="415b2-156">Typecasting the result lets the compiler know you are sure about the result.</span></span> <span data-ttu-id="415b2-157">Detto questo, assicurarsi di avere compreso il calcolo e di essere in grado di rientrare in un **ULONG** a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="415b2-157">That being said, make certain you understand the calculation and really are sure it will fit in a 32-bit **ULONG**.</span></span>

<span data-ttu-id="415b2-158">Se il risultato potrebbe non rientrare in un **ULONG** a 32 bit, modificare il tipo di base della variabile che conterrà il risultato.</span><span class="sxs-lookup"><span data-stu-id="415b2-158">If the result may not fit in a 32-bit **ULONG**, change the base type of the variable that will hold the result.</span></span>

</dd> </dl>

## <a name="warning-c4311---example-1"></a><span data-ttu-id="415b2-159">Avviso C4311-esempio 1</span><span class="sxs-lookup"><span data-stu-id="415b2-159">Warning C4311 - Example 1</span></span>

<span data-ttu-id="415b2-160">' Type cast ': troncamento puntatore da' void \* \_ \_ ptr64' a' unsigned long '</span><span class="sxs-lookup"><span data-stu-id="415b2-160">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="415b2-161"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Codice</span><span class="sxs-lookup"><span data-stu-id="415b2-161"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
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

<span data-ttu-id="415b2-162"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione</span><span class="sxs-lookup"><span data-stu-id="415b2-162"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="415b2-163">Questa funzione completa gestisce gli indirizzi come numeri interi, rendendo necessaria la necessità di digitare tali numeri interi in modo portatile.</span><span class="sxs-lookup"><span data-stu-id="415b2-163">This entire function deals with addresses as integers, necessitating the need to type those integers in a portable way.</span></span> <span data-ttu-id="415b2-164">Tutte le variabili locali, i valori intermedi nei calcoli e i valori restituiti devono essere tipi portabili.</span><span class="sxs-lookup"><span data-stu-id="415b2-164">All the local variables, intermediate values in calculations, and return values should be portable types.</span></span>

</dd> <dt>

<span data-ttu-id="415b2-165"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluzione</span><span class="sxs-lookup"><span data-stu-id="415b2-165"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
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

<span data-ttu-id="415b2-166">**PULONG \_ PTR** è un puntatore che si trova a 32 bit per Windows a 32 bit e 64 bit per Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="415b2-166">**PULONG\_PTR** is a pointer that is itself 32 bits for 32-bit Windows and 64 bits for 64-bit Windows.</span></span> <span data-ttu-id="415b2-167">Punta a un Unsigned Integer, **ULONG \_ ptr**, che è 32 bit per Windows a 32 bit e 64 bit per Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="415b2-167">It points to an unsigned integer, **ULONG\_PTR**, that is 32 bits for 32-bit Windows and 64 bits for 64-bit Windows.</span></span>

</dd> </dl>

## <a name="warning-c4311---example-2"></a><span data-ttu-id="415b2-168">Avviso C4311-esempio 2</span><span class="sxs-lookup"><span data-stu-id="415b2-168">Warning C4311 - Example 2</span></span>

<span data-ttu-id="415b2-169">' Type cast ': troncamento puntatore da' void \* \_ \_ ptr64' a' unsigned long '</span><span class="sxs-lookup"><span data-stu-id="415b2-169">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="415b2-170"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Codice</span><span class="sxs-lookup"><span data-stu-id="415b2-170"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
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

<span data-ttu-id="415b2-171"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione</span><span class="sxs-lookup"><span data-stu-id="415b2-171"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="415b2-172">Anche se tutti i valori di QVA (quasi Virtual Address) sono effettivamente valori a 32 bit in questa fase e si adattano a un **ULONG**, è più coerente considerare tutti gli indirizzi come valori **\_ ptr ULONG** , quando possibile.</span><span class="sxs-lookup"><span data-stu-id="415b2-172">Even though all QVA (Quasi Virtual Address) values are really 32-bit values at this stage and will fit in a **ULONG**, it is more consistent to treat all addresses as **ULONG\_PTR** values when possible.</span></span>

<span data-ttu-id="415b2-173">Il puntatore PciIoSpaceBase include il QVA creato nella macro HAL \_ make \_ QVA.</span><span class="sxs-lookup"><span data-stu-id="415b2-173">The pointer PciIoSpaceBase holds the QVA that is created in the macro HAL\_MAKE\_QVA.</span></span> <span data-ttu-id="415b2-174">Questa macro restituisce un valore a 64 bit con i primi 32 bit impostati su zero, in modo che la matematica funzionerà.</span><span class="sxs-lookup"><span data-stu-id="415b2-174">This macro returns a 64-bit value with the top 32 bits set to zero so the math will work.</span></span> <span data-ttu-id="415b2-175">È possibile lasciare semplicemente il codice per troncare il puntatore in un **ULONG**, ma questa pratica è sconsigliata per migliorare la gestibilità e la portabilità del codice.</span><span class="sxs-lookup"><span data-stu-id="415b2-175">We could simply leave the code to truncate the pointer into a **ULONG**, but this practice is discouraged to enhance code maintainability and portability.</span></span> <span data-ttu-id="415b2-176">Ad esempio, il contenuto di un QVA potrebbe cambiare in futuro per usare alcuni dei bit superiori a questo livello, suddividendo il codice.</span><span class="sxs-lookup"><span data-stu-id="415b2-176">For example, the contents of a QVA might change in the future to use some of the upper bits at this level, breaking the code.</span></span>

</dd> <dt>

<span data-ttu-id="415b2-177"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluzione</span><span class="sxs-lookup"><span data-stu-id="415b2-177"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="415b2-178">Essere sicuri e usare **il \_ ptr ULONG** per tutti gli indirizzi e i calcoli matematici.</span><span class="sxs-lookup"><span data-stu-id="415b2-178">Be safe and use **ULONG\_PTR** for all address and pointer math.</span></span>

`HalpCMOSRamBase = (PVOID)((ULONG_PTR)PciIoSpaceBase + CMOS_ISA_PORT_ADDRESS);`

</dd> </dl>

## <a name="warning-c4311-example-3"></a><span data-ttu-id="415b2-179">Esempio di C4311 di avviso 3</span><span class="sxs-lookup"><span data-stu-id="415b2-179">Warning C4311 Example 3</span></span>

<span data-ttu-id="415b2-180">' Type cast ': troncamento puntatore da' void \* \_ \_ ptr64' a' unsigned long '</span><span class="sxs-lookup"><span data-stu-id="415b2-180">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="415b2-181"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Codice</span><span class="sxs-lookup"><span data-stu-id="415b2-181"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
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

<span data-ttu-id="415b2-182"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione</span><span class="sxs-lookup"><span data-stu-id="415b2-182"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="415b2-183">Il compilatore genera un avviso sull'indirizzo degli operatori (&) e di spostamento a sinistra (<<) se vengono applicati ai tipi di puntatore.</span><span class="sxs-lookup"><span data-stu-id="415b2-183">The compiler warns about the address of (&) and left shift (<<) operators if they are applied to pointer types.</span></span> <span data-ttu-id="415b2-184">Nel codice precedente, QVA è un valore **PVOID** .</span><span class="sxs-lookup"><span data-stu-id="415b2-184">In the above code, Qva is a **PVOID** value.</span></span> <span data-ttu-id="415b2-185">È necessario eseguirne il cast a un tipo integer per eseguire la matematica.</span><span class="sxs-lookup"><span data-stu-id="415b2-185">We need to cast that to an integer type to perform the math.</span></span> <span data-ttu-id="415b2-186">Poiché il codice deve essere portabile, utilizzare **ULONG \_ ptr** anziché **ULONG**.</span><span class="sxs-lookup"><span data-stu-id="415b2-186">Because the code must be portable, use **ULONG\_PTR** instead of **ULONG**.</span></span>

</dd> <dt>

<span data-ttu-id="415b2-187"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluzione</span><span class="sxs-lookup"><span data-stu-id="415b2-187"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

``` syntax
if ( ((ULONG_PTR) Qva & QVA_SELECTORS) == QVA_ENABLE ) {
  return( (PVOID)( (ULONG_PTR)Qva << IO_BIT_SHIFT ) );
```

</dd> </dl>

## <a name="warning-c4311-example-4"></a><span data-ttu-id="415b2-188">Avviso C4311 esempio 4</span><span class="sxs-lookup"><span data-stu-id="415b2-188">Warning C4311 Example 4</span></span>

<span data-ttu-id="415b2-189">' Type cast ': troncamento puntatore da' void \* \_ \_ ptr64' a' unsigned long '</span><span class="sxs-lookup"><span data-stu-id="415b2-189">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="415b2-190"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Codice</span><span class="sxs-lookup"><span data-stu-id="415b2-190"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

``` syntax
TranslatedAddress->LowPart = (ULONG)HalCreateQva(
*TranslatedAddress, va);
```

</dd> <dt>

<span data-ttu-id="415b2-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione</span><span class="sxs-lookup"><span data-stu-id="415b2-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="415b2-192">TranslatedAddress è un'Unione che ha un aspetto simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="415b2-192">TranslatedAddress is a union that looks something like the following:</span></span>

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

<span data-ttu-id="415b2-193"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluzione</span><span class="sxs-lookup"><span data-stu-id="415b2-193"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="415b2-194">Conoscendo il resto del codice potrebbe essere inserito in HighPart, è possibile selezionare una delle soluzioni illustrate qui.</span><span class="sxs-lookup"><span data-stu-id="415b2-194">Knowing what the rest of the code might place in Highpart, we can select either of the solutions shown here.</span></span>

`TranslatedAddress->LowPart = PtrToUlong(HalCreateQva(*TranslatedAddress,va) );`

<span data-ttu-id="415b2-195">La macro **PtrToUlong** tronca il puntatore restituito da **HalCreateQva** a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="415b2-195">The **PtrToUlong** macro truncates the pointer returned by **HalCreateQva** to 32 bits.</span></span> <span data-ttu-id="415b2-196">Sappiamo che QVA restituito da **HalCreateQva** ha i bit 32 superiori impostati su zero e la riga di codice successiva imposta TranslatedAddress->HighPart su zero.</span><span class="sxs-lookup"><span data-stu-id="415b2-196">We know that the QVA returned by **HalCreateQva** has the upper 32 bits set to zero and the very next line of code sets TranslatedAddress->Highpart to zero.</span></span>

<span data-ttu-id="415b2-197">Con cautela, è possibile usare gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="415b2-197">With caution, we could use the following:</span></span>

`TranslatedAddress->QuadPart = (LONGLONG)HalCreateQva(*TranslatedAddress,va);`

<span data-ttu-id="415b2-198">Questa operazione funziona in questo esempio: la macro **HalCreateQva** restituisce 64 bit, con i bit 32 superiore impostati su zero.</span><span class="sxs-lookup"><span data-stu-id="415b2-198">This works in this example: the **HalCreateQva** macro is returning 64 bits, with the upper 32 bits set to zero.</span></span> <span data-ttu-id="415b2-199">È sufficiente evitare di lasciare invariati i 32 bit superiori in un ambiente a 32 bit, che la seconda soluzione può effettivamente eseguire.</span><span class="sxs-lookup"><span data-stu-id="415b2-199">Just be careful not to leave the upper 32 bits undefined in a 32-bit environment, which this second solution may actually do.</span></span>

</dd> </dl>

## <a name="warning-c4311-example-5"></a><span data-ttu-id="415b2-200">Avviso C4311 esempio 5</span><span class="sxs-lookup"><span data-stu-id="415b2-200">Warning C4311 Example 5</span></span>

<span data-ttu-id="415b2-201">' Type cast ': troncamento puntatore da' void \* \_ \_ ptr64' a' unsigned long '</span><span class="sxs-lookup"><span data-stu-id="415b2-201">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="415b2-202"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Codice</span><span class="sxs-lookup"><span data-stu-id="415b2-202"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
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

<span data-ttu-id="415b2-203"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione</span><span class="sxs-lookup"><span data-stu-id="415b2-203"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="415b2-204">WindowRegisters->WindowBase è un puntatore e ora è 64 bit.</span><span class="sxs-lookup"><span data-stu-id="415b2-204">WindowRegisters->WindowBase is a pointer and is now 64 bits.</span></span> <span data-ttu-id="415b2-205">Il codice dice di spostare a destra questo valore di 20 bit.</span><span class="sxs-lookup"><span data-stu-id="415b2-205">The code says to right-shift this value 20 bits.</span></span> <span data-ttu-id="415b2-206">Il compilatore non consentirà di usare l'operatore di spostamento a destra (>>) su un puntatore. Pertanto, è necessario eseguirne il cast a un tipo Integer.</span><span class="sxs-lookup"><span data-stu-id="415b2-206">The compiler will not let us use the right-shift (>>) operator on a pointer; therefore, we need to cast it to some sort of integer.</span></span>

</dd> <dt>

<span data-ttu-id="415b2-207"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Soluzione</span><span class="sxs-lookup"><span data-stu-id="415b2-207"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

`Wbase.Wbase= PtrToUlong ( (PVOID) ((ULONG_PTR) (WindowRegisters->WindowBase) >> 20));`

<span data-ttu-id="415b2-208">Il cast a **un \_ ptr ULONG** è solo quello che serve.</span><span class="sxs-lookup"><span data-stu-id="415b2-208">Casting to a **ULONG\_PTR** is just what we need.</span></span> <span data-ttu-id="415b2-209">Il problema successivo è wbase.</span><span class="sxs-lookup"><span data-stu-id="415b2-209">The next problem is Wbase.</span></span> <span data-ttu-id="415b2-210">Wbase è un **ULONG** e è 32 bit.</span><span class="sxs-lookup"><span data-stu-id="415b2-210">Wbase is a **ULONG** and is 32 bits.</span></span> <span data-ttu-id="415b2-211">In questo caso, è noto che il puntatore a 64 bit WindowRegisters->WindowBase è valido nei 32 bit inferiori anche dopo essere stato spostato.</span><span class="sxs-lookup"><span data-stu-id="415b2-211">In this case, we know that the 64-bit pointer WindowRegisters->WindowBase is valid in the lower 32 bits even after being shifted.</span></span> <span data-ttu-id="415b2-212">In questo modo si usa la macro **PtrToUlong** accettabile, perché tronca il puntatore a 64 bit in un **ULONG** a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="415b2-212">This makes use of the **PtrToUlong** macro acceptable, because it will truncate the 64-bit pointer into a 32-bit **ULONG**.</span></span> <span data-ttu-id="415b2-213">Il cast **PVOID** è necessario perché **PtrToUlong** prevede un argomento puntatore.</span><span class="sxs-lookup"><span data-stu-id="415b2-213">The **PVOID** cast is necessary because **PtrToUlong** expects a pointer argument.</span></span> <span data-ttu-id="415b2-214">Quando si esamina il codice assembler risultante, tutto questo cast del codice C diventa solo un quad di carico, uno spostamento a destra e un archivio lungo.</span><span class="sxs-lookup"><span data-stu-id="415b2-214">When you look at the resulting assembler code, all this C code casting becomes just a load quad, shift right, and store long.</span></span>

</dd> </dl>

 

 




