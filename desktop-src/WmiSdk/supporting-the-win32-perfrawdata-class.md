---
description: Quando si scrive un provider ad alte prestazioni che deriva classi da Win32 PerfRawData, è necessario seguire convenzioni specifiche in modo che WMI possa fornire dati ai valori \_ delle proprietà.
ms.assetid: 04abb2f9-800f-497a-ac8f-8ef210746273
ms.tgt_platform: multiple
title: Supporto della classe Win32_PerfRawData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70c9899c88849c70265b019c1d73021c61cae4758c41f462349537bd2e806ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050119"
---
# <a name="supporting-the-win32_perfrawdata-class"></a>Supporto della classe \_ PerfRawData Win32

Quando si scrive un provider ad alte prestazioni che deriva classi da [**\_ Win32 PerfRawData,**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)è necessario seguire convenzioni specifiche in modo che WMI possa fornire dati ai valori delle proprietà.

> [!Note]  
> La scrittura di un provider WMI ad alte prestazioni per la creazione di contatori delle prestazioni non è consigliata in alcuna versione del Windows operativo. Per altre informazioni, vedere [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md)and Performance Libraries and [WMI](performance-libraries-and-wmi.md).

 

La procedura seguente descrive come supportare la [**classe \_ Win32 PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) con il provider ad alte prestazioni.

**Per supportare la classe \_ PerfRawData Win32**

1.  Creare la classe nello spazio dei \\ nomi CIMv2 radice.

    La classe deve essere derivata da [**\_ Win32 PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e il qualificatore **Hiperf** deve essere impostato su **TRUE.** È anche possibile aggiungere classi di dati sulle prestazioni WDM (driver) allo spazio dei nomi \\ WMI radice. Per altre informazioni sulla creazione di una classe personalizzata per WMI, vedere [Progettazione di Managed Object Format (MOF).](designing-managed-object-format--mof--classes.md)

2.  Specificare il provider come "NT5 \_ GenericPerfProvider \_ V1" nel **qualificatore provider.**
3.  Specificare i qualificatori a livello di classe seguenti:

    -   **HiPerf**
    -   **Impostazioni locali**
    -   **PerfDetail**
    -   **Provider**

    Per altre informazioni, vedere [**Qualificatori di classe per le classi dei contatori delle prestazioni.**](class-qualifiers-for-performance-counter-classes.md) Non definire il **qualificatore GenericPerfCtr** perché è riservato al processo ADAP che trasferisce i dati della libreria delle prestazioni nelle classi WMI.

4.  Popolare le proprietà di timestamp e frequenza appropriate usate per calcolare le formule di tipo contatore.

    Queste proprietà vengono ereditate da [**\_ Win32 PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e, se si scrive un provider ad alte prestazioni, è necessario compilarlo per visualizzare la classe in Monitoraggio di sistema.

5.  Includere una proprietà chiave denominata **Name** nella classe (questa proprietà non è necessaria per le classi singleton).

    Non è necessario usare alcuna proprietà chiave diversa da **Name** nella classe.

6.  Creare proprietà con tipi di dati **DWORD** (**uint32**) o **QWORD** (**uint64**). Queste proprietà diventano contatori delle prestazioni quando vengono trasferite alle librerie delle prestazioni.
7.  Specificare i qualificatori a livello di proprietà seguenti per tutte le proprietà nella classe:

    -   **DisplayName**
    -   **CounterType**
    -   **DefaultScale**
    -   **Descrizione**
    -   **PerfDefault**
    -   **PerfDetail**

    Per altre informazioni, vedere [**Qualificatori di proprietà per le classi dei contatori delle prestazioni.**](property-qualifiers-for-performance-counter-classes.md) Inoltre, il file di intestazione Winperf.h contiene valori che è possibile specificare per **PerfDetail** e **CounterType**.

    WMI usa i **qualificatori DisplayName,** **Locale** **e Description** per la localizzazione. È necessario aggiungere qualificatori modificati allo spazio dei nomi MS 409 (inglese) in modo che Monitoraggio di sistema possa \_ visualizzare correttamente i dati della classe. Ciò significa che è possibile modificare la definizione della proprietà aggiungendo un qualificatore **Description** con testo esplicativo e compilare il **valore DisplayName.** È inoltre necessario aggiungere qualificatori modificati a qualsiasi altro spazio dei nomi delle impostazioni locali che la classe supporta. Se un utente richiede dati da impostazioni locali per cui non si specificano qualificatori modificati, WMI per impostazione predefinita viene utilizzato per le definizioni specificate nello spazio dei nomi MS \_ 409.

8.  Creare una proprietà di base per qualsiasi proprietà con un tipo di contatore che prevede un valore di base.

    Questa proprietà segue immediatamente la proprietà ed è denominata *propertyname***\_ Base**. Ad esempio, la proprietà media **AvgDiskBytesPerRead** nella classe [**\_ PerfRawData \_ PerfDisk \_ LogicalDisk di Win32**](./retrieving-raw-and-formatted-performance-data.md) richiede una proprietà di base denominata **AvgDiskBytesPerRead \_ Base** per contare il numero di campioni. Per determinare se il tipo di contatore che si desidera utilizzare richiede una proprietà di base, individuare il tipo di contatore in base al nome o al valore decimale in [Wmi Performance Counter Types](wmi-performance-counter-types.md).

9.  Assicurarsi che il provider soddisfi i [requisiti di prestazioni](supporting-the-win32-perfformatteddata-class.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un provider di istanze in un provider High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
