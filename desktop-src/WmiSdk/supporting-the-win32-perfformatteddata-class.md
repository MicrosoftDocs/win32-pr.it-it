---
description: Quando si scrive un provider a prestazioni elevate che deriva classi da Win32 \_ PerfFormattedData, è necessario seguire convenzioni specifiche, in modo che WMI possa calcolare i valori delle proprietà.
ms.assetid: 57912f6f-45ca-491c-8a6c-77e2a6937ccc
ms.tgt_platform: multiple
title: Supporto della classe Win32_PerfFormattedData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54911105f5c485d3a80ddb93b96f0af2637c9506
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317546"
---
# <a name="supporting-the-win32_perfformatteddata-class"></a>Supporto della \_ classe Win32 PerfFormattedData

Quando si scrive un provider a prestazioni elevate che deriva classi da [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), è necessario seguire convenzioni specifiche, in modo che WMI possa calcolare i valori delle proprietà.

> [!Note]  
> La scrittura di un provider WMI a prestazioni elevate per la creazione di contatori delle prestazioni non è consigliata in alcuna versione del sistema operativo Windows. Per ulteriori informazioni, vedere la pagina relativa alla creazione di un [provider di istanze in un provider High-Performance e in](making-an-instance-provider-into-a-high-performance-provider.md)librerie di [prestazioni e WMI](performance-libraries-and-wmi.md).

 

Nella procedura riportata di seguito viene descritto come supportare la \_ classe Win32 PerfFormattedData.

**Per supportare la \_ classe Win32 PerfFormattedData**

1.  Creare la classe nello stesso spazio dei nomi della classe RAW corrispondente. La classe deve essere derivata da [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) e il qualificatore **HiPerf** è impostato su **true**. Per ulteriori informazioni sulla creazione di una classe personalizzata per WMI, vedere [progettazione di classi Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).
2.  Specificare "HiPerfCooker \_ V1" nel qualificatore del [**provider**](class-qualifiers-for-performance-counter-classes.md) .
3.  Specificare i qualificatori a livello di classe seguenti oltre ai qualificatori utilizzati per le classi non elaborate:

    -   [**Autocook**](class-qualifiers-for-performance-counter-classes.md)
    -   [**RawClass autocook \_**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Cotto**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Costose**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Dinamico**](dynamic-qualifier.md)
    -   [**HiPerf**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Locale**](class-qualifiers-for-performance-counter-classes.md)
    -   [**PerfDefault**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Provider**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Singleton**](standard-wmi-qualifiers.md)

    > [!Note]  
    > Non impostare alcun valore per **GenericPerfCtr**, **PerfIndex** o **HelpIndex** perché verranno impostati dal processo ADAP. Per ulteriori informazioni, vedere [**qualificatori di classe per le classi dei contatori delle prestazioni**](class-qualifiers-for-performance-counter-classes.md).

     

4.  Includere una proprietà chiave denominata **Name** nella classe (questa proprietà non è obbligatoria per le classi singleton).

    Il valore della proprietà **Name** deve essere uguale a quello della classe RAW corrispondente. Non è necessario usare alcuna proprietà chiave diversa da **Name** nella classe.

5.  Creare i dati delle proprietà digitati come **DWORD** (**UInt32**) o **QWORD** (**UInt64**).

    Le proprietà devono corrispondere a una proprietà nella classe RAW o a una proprietà nella classe che si sta creando.

6.  Specificare i seguenti qualificatori a livello di proprietà per tutte le proprietà della classe, oltre ai qualificatori **PerfIndex** e **PerfDetail** usati per le proprietà della classe RAW:

    -   [**Base**](property-qualifiers-for-performance-counter-classes.md)
    -   [**CookingType**](property-qualifiers-for-performance-counter-classes.md)
    -   [**Contatore**](property-qualifiers-for-performance-counter-classes.md)
    -   [**PerfTimeStamp**](property-qualifiers-for-performance-counter-classes.md)
    -   [**PerfTimeFreq**](property-qualifiers-for-performance-counter-classes.md)
    -   [**SampleWindow**](property-qualifiers-for-performance-counter-classes.md)

    Per ulteriori informazioni, vedere [**qualificatori di proprietà per le classi dei contatori delle prestazioni**](property-qualifiers-for-performance-counter-classes.md). Il file di intestazione Winperf. h contiene inoltre valori che è possibile specificare per **PerfDetail** e **CounterType**.

7.  Verificare che il provider soddisfi i [requisiti di prestazioni](#performance-requirements).

## <a name="performance-requirements"></a>Requisiti relativi alle prestazioni

Quando si scrive un provider a prestazioni elevate, le prestazioni devono soddisfare i requisiti seguenti:

-   L'apertura del file DLL a prestazioni elevate non può richiedere più di 100 millisecondi. In generale, l'apertura di ciascun provider a prestazioni elevate e la libreria delle prestazioni non può superare i 5 secondi.
-   L'aggiornamento dati non può richiedere più di 10 millisecondi per ogni raccolta. In un'operazione di aggiornamento e raccolta complessiva tutti i provider a prestazioni elevate insieme non possono richiedere più di 800 millisecondi.
-   Il carico complessivo della CPU per tutti i provider a prestazioni elevate non può superare il 6-7% di overhead della CPU o il 5% per la registrazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un provider di istanze in un provider di High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
