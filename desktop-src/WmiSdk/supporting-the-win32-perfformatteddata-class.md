---
description: Quando si scrive un provider ad alte prestazioni che deriva classi da Win32 PerfFormattedData, è necessario seguire convenzioni specifiche in modo che WMI possa calcolare i valori \_ delle proprietà.
ms.assetid: 57912f6f-45ca-491c-8a6c-77e2a6937ccc
ms.tgt_platform: multiple
title: Supporto della classe Win32_PerfFormattedData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bbed50bde7ef16f6362d28151744cf22d66e5d0f56df253ad48ab469b397d0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050129"
---
# <a name="supporting-the-win32_perfformatteddata-class"></a>Supporto della classe \_ PerfFormattedData Win32

Quando si scrive un provider ad alte prestazioni che deriva classi da [**Win32 \_ PerfFormattedData,**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)è necessario seguire convenzioni specifiche in modo che WMI possa calcolare i valori delle proprietà.

> [!Note]  
> La scrittura di un provider WMI ad alte prestazioni per creare contatori delle prestazioni non è consigliata in nessuna versione del Windows operativo. Per altre informazioni, vedere [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md)and Performance Libraries and [WMI](performance-libraries-and-wmi.md).

 

La procedura seguente descrive come supportare la classe \_ Win32 PerfFormattedData.

**Per supportare la classe \_ Win32 PerfFormattedData**

1.  Creare la classe nello stesso spazio dei nomi della classe non elaborata corrispondente. La classe deve essere derivata da [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) e il qualificatore **HiPerf** deve essere impostato su **TRUE.** Per altre informazioni sulla creazione di una classe personalizzata per WMI, vedere [Progettazione di Managed Object Format (MOF).](designing-managed-object-format--mof--classes.md)
2.  Specificare "HiPerfCooker \_ v1" nel [**qualificatore provider.**](class-qualifiers-for-performance-counter-classes.md)
3.  Specificare i qualificatori a livello di classe seguenti oltre ai qualificatori usati per le classi non elaborate:

    -   [**AutoCook**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Autocook \_ RawClass**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Cucinato**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Costoso**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Dinamico**](dynamic-qualifier.md)
    -   [**HiPerf**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Locale**](class-qualifiers-for-performance-counter-classes.md)
    -   [**PerfDefault**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Provider**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Singleton**](standard-wmi-qualifiers.md)

    > [!Note]  
    > Non impostare alcun valore per **GenericPerfCtr,** **PerfIndex** o **HelpIndex** perché verranno impostati dal processo ADAP. Per altre informazioni, vedere [**Qualificatori di classe per le classi dei contatori delle prestazioni**](class-qualifiers-for-performance-counter-classes.md).

     

4.  Includere una proprietà chiave denominata **Name** nella classe (questa proprietà non è necessaria per le classi singleton).

    Il valore della **proprietà Name** deve corrispondere alla classe non elaborata corrispondente. Non è necessario usare alcuna proprietà chiave diversa **da Name** nella classe.

5.  Creare i dati delle proprietà digitati **come DWORD** (**uint32**) o **QWORD** (**uint64**).

    Le proprietà devono corrispondere a una proprietà nella classe non elaborata o a una proprietà nella classe che si sta creando.

6.  Specificare i qualificatori a livello di proprietà seguenti per tutte le proprietà della classe oltre ai qualificatori **PerfIndex** e **PerfDetail** usati per le proprietà della classe non elaborata:

    -   [**Base**](property-qualifiers-for-performance-counter-classes.md)
    -   [**Tipo di cucina**](property-qualifiers-for-performance-counter-classes.md)
    -   [**Contatore**](property-qualifiers-for-performance-counter-classes.md)
    -   [**PerfTimeStamp**](property-qualifiers-for-performance-counter-classes.md)
    -   [**PerfTimeFreq**](property-qualifiers-for-performance-counter-classes.md)
    -   [**SampleWindow**](property-qualifiers-for-performance-counter-classes.md)

    Per altre informazioni, vedere [**Qualificatori di proprietà per le classi dei contatori delle prestazioni**](property-qualifiers-for-performance-counter-classes.md). Inoltre, il file di intestazione Winperf.h contiene valori che è possibile specificare per **PerfDetail** **e CounterType.**

7.  Assicurarsi che il provider soddisfi i [requisiti di prestazioni](#performance-requirements).

## <a name="performance-requirements"></a>Requisiti di prestazioni

Quando si scrive un provider ad alte prestazioni, le relative prestazioni devono soddisfare i requisiti seguenti:

-   L'apertura del file DLL ad alte prestazioni può richiedere non più di 100 millisecondi. In generale, l'apertura di ogni provider a prestazioni elevate e della libreria delle prestazioni non può superare i 5 secondi.
-   L'aggiornamento dei dati può richiedere non più di 10 millisecondi per ogni raccolta. In un'operazione di aggiornamento e raccolta complessiva, tutti i provider ad alte prestazioni insieme non possono richiedere più di 800 millisecondi.
-   Il carico complessivo della CPU per tutti i provider ad alte prestazioni non può superare il 6-7% in modo interattivo o il 5% per la registrazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un provider di istanze in un provider di High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
