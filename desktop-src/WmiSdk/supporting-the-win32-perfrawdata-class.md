---
description: Quando si scrive un provider a prestazioni elevate che deriva classi da Win32 \_ PerfRawData, è necessario seguire convenzioni specifiche, in modo che WMI possa fornire dati ai valori delle proprietà.
ms.assetid: 04abb2f9-800f-497a-ac8f-8ef210746273
ms.tgt_platform: multiple
title: Supporto della classe Win32_PerfRawData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 835815c9171097bfe088d22e4154ac668d790c0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309870"
---
# <a name="supporting-the-win32_perfrawdata-class"></a>Supporto della \_ classe Win32 PerfRawData

Quando si scrive un provider a prestazioni elevate che deriva classi da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata), è necessario seguire convenzioni specifiche, in modo che WMI possa fornire dati ai valori delle proprietà.

> [!Note]  
> La scrittura di un provider WMI a prestazioni elevate per la creazione di contatori delle prestazioni non è consigliata in alcuna versione del sistema operativo Windows. Per ulteriori informazioni, vedere la pagina relativa alla creazione di un [provider di istanze in un provider High-Performance e in](making-an-instance-provider-into-a-high-performance-provider.md)librerie di [prestazioni e WMI](performance-libraries-and-wmi.md).

 

Nella procedura riportata di seguito viene descritto come supportare la classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) con il provider a prestazioni elevate.

**Per supportare la \_ classe Win32 PerfRawData**

1.  Creare la classe nello \\ spazio dei nomi CIMv2 radice.

    La classe deve essere derivata da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e il qualificatore **HiPerf** è impostato su **true**. È inoltre possibile aggiungere classi di dati sulle prestazioni WDM (driver) allo \\ spazio dei nomi WMI radice. Per ulteriori informazioni sulla creazione di una classe personalizzata per WMI, vedere [progettazione di classi Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).

2.  Specificare il provider come "NT5 \_ GenericPerfProvider \_ V1" nel qualificatore del **provider** .
3.  Specificare i qualificatori a livello di classe seguenti:

    -   **HiPerf**
    -   **Impostazioni locali**
    -   **PerfDetail**
    -   **Provider**

    Per ulteriori informazioni, vedere [**qualificatori di classe per le classi dei contatori delle prestazioni**](class-qualifiers-for-performance-counter-classes.md). Non definire il qualificatore **GenericPerfCtr** perché è riservato per il processo ADAP che trasferisce i dati della libreria delle prestazioni in classi WMI.

4.  Popola le proprietà timestamp e Frequency appropriate utilizzate per calcolare le formule di tipo contatore.

    Queste proprietà vengono ereditate da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e, se si sta scrivendo un provider a prestazioni elevate, è necessario compilare tali proprietà affinché la classe venga visualizzata in Monitor di sistema.

5.  Includere una proprietà chiave denominata **Name** nella classe (questa proprietà non è obbligatoria per le classi singleton).

    Non è necessario usare alcuna proprietà chiave diversa da **Name** nella classe.

6.  Crea proprietà dati tipizzati come **DWORD** (**UInt32**) o **QWORD** (**UInt64**). Queste proprietà diventano contatori delle prestazioni quando vengono trasferite alle librerie delle prestazioni.
7.  Specificare i seguenti qualificatori a livello di proprietà per tutte le proprietà della classe:

    -   **DisplayName**
    -   **CounterType**
    -   **DefaultScale**
    -   **Descrizione**
    -   **PerfDefault**
    -   **PerfDetail**

    Per ulteriori informazioni, vedere [**qualificatori di proprietà per le classi dei contatori delle prestazioni**](property-qualifiers-for-performance-counter-classes.md). Il file di intestazione Winperf. h contiene inoltre valori che è possibile specificare per **PerfDetail** e **CounterType**.

    WMI utilizza i qualificatori **DisplayName**, **locale** e **Description** per la localizzazione. È necessario aggiungere i qualificatori modificati allo \_ spazio dei nomi MS 409 (Inglese) in modo che monitor di sistema possa visualizzare correttamente i dati della classe. Ciò significa che è possibile modificare la definizione della proprietà aggiungendo un qualificatore di **Descrizione** con il testo esplicativo e compilare il valore **DisplayName** . È inoltre necessario aggiungere qualificatori modificati a qualsiasi altro spazio dei nomi delle impostazioni locali supportato dalla classe. Se un utente richiede dati da impostazioni locali per le quali non si forniscono qualificatori corretti, WMI utilizza per impostazione predefinita le definizioni specificate nello \_ spazio dei nomi MS 409.

8.  Creare una proprietà di base per qualsiasi proprietà che dispone di un tipo di contatore che prevede un valore di base.

    Questa proprietà segue immediatamente la proprietà ed è denominata * propertyName ***\_ base**. Ad esempio, la proprietà media **AvgDiskBytesPerRead** della classe [**Win32 \_ PerfRawData \_ perfdisk \_ disco logico**](./retrieving-raw-and-formatted-performance-data.md) richiede una proprietà di base denominata **AvgDiskBytesPerRead \_ base** per contare il numero di campioni. Per determinare se il tipo di contatore che si desidera utilizzare richiede una proprietà di base, individuare il tipo di contatore in base al nome o al valore decimale nei [tipi di contatori delle prestazioni WMI](wmi-performance-counter-types.md).

9.  Verificare che il provider soddisfi i [requisiti di prestazioni](supporting-the-win32-perfformatteddata-class.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un provider di istanze in un provider di High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
