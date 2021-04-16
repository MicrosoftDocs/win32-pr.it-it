---
description: WMI fornisce un'interfaccia uniforme per tutte le applicazioni locali o remote o script che ottengono dati di gestione da un sistema di computer, una rete o un'azienda.
ms.assetid: 41ba2a64-3322-48b8-a6ea-e468bfac06e2
ms.tgt_platform: multiple
title: Architettura WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b90ee4f81c2afdfc222dd7d5d824f88bda122b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104562742"
---
# <a name="wmi-architecture"></a>Architettura WMI

WMI fornisce un'interfaccia uniforme per tutte le applicazioni locali o remote o script che ottengono dati di gestione da un sistema di computer, una rete o un'azienda. L'interfaccia uniforme è progettata in modo che le applicazioni e gli script client WMI non debbano chiamare un'ampia gamma di API (Application Programming Interface) del sistema operativo. Molte API non possono essere chiamate da client di automazione come script o applicazioni Visual Basic. Altre API non eseguono chiamate a computer remoti.

Per ottenere dati da WMI, scrivere uno script client o un'applicazione che accede a [classi WMI](wmi-classes.md) o fornire dati a WMI scrivendo un [*provider WMI*](gloss-p.md). Per ulteriori informazioni, vedere [utilizzo di WMI](using-wmi.md).

## <a name="objects-consumers-and-infrastructure-of-wmi"></a>Oggetti, consumer e infrastruttura di WMI

Nel diagramma seguente viene illustrata la relazione tra l'infrastruttura WMI e i provider WMI e gli oggetti gestiti e viene inoltre illustrata la relazione tra l'infrastruttura WMI e i consumer WMI.

![relazione tra l'infrastruttura WMI, i provider WMI e gli oggetti gestiti](images/wmi-architecture.png)

## <a name="wmi-components"></a>Componenti WMI

Nell'elenco seguente vengono descritti i principali componenti WMI:

-   Oggetti gestiti e provider WMI

    Un provider WMI è un oggetto COM che monitora uno o più [*oggetti gestiti*](gloss-m.md) per WMI. Un oggetto gestito è un componente aziendale logico o fisico, ad esempio un'unità disco rigido, una scheda di rete, un sistema di database, un sistema operativo, un processo o un servizio.

    Analogamente a un driver, un provider fornisce WMI con dati da un oggetto gestito e gestisce i messaggi da WMI all'oggetto gestito. I provider WMI sono costituiti da un file DLL e da un file [*Managed Object Format (MOF)*](gloss-m.md) che definisce le classi per le quali il provider restituisce i dati ed esegue operazioni. I provider, come le applicazioni WMI C++, usano l' [API com per WMI](com-api-for-wmi.md). Per ulteriori informazioni, vedere la pagina relativa [alla fornitura di dati a WMI](providing-data-to-wmi.md).

    Un esempio di provider è il [provider del registro](/previous-versions/windows/desktop/regprov/system-registry-provider)preinstallato, che accede ai dati nel registro di sistema. Il provider del registro di sistema dispone di una [*classe WMI*](gloss-w.md), [**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), con molti metodi ma senza proprietà. Altri provider preinstallati, ad esempio il [provider Win32](/windows/desktop/CIMWin32Prov/win32-provider), dispongono in genere di classi con molte proprietà ma con pochi metodi, come il [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) o [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk). Il file DLL del provider del registro di sistema, Stdprov.dll, contiene il codice che restituisce dinamicamente i dati quando richiesto dagli script client o dalle applicazioni.

    I file MOF e DLL di WMI si trovano in% WINDIR% \\ system32 \\ WBEM, insieme agli [strumenti di Command-Line WMI](wmi-command-line-tools.md), ad esempio [**Winmgmt.exe**](winmgmt.md) e [**Mofcomp.exe**](mofcomp.md). Le classi provider, ad esempio [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), sono definite nei file MOF e quindi compilate nel repository WMI all'avvio del sistema.

-   [Infrastruttura WMI](wmi-infrastructure.md)

    L'infrastruttura WMI è un componente del sistema operativo Microsoft Windows noto come servizio WMI (Winmgmt). L'infrastruttura WMI è costituita da due componenti: il nucleo WMI e il [*repository WMI*](gloss-w.md).

    Il repository WMI è organizzato in base agli [*spazi dei nomi*](gloss-n.md)WMI. Il servizio WMI crea alcuni spazi dei nomi, ad esempio radice radice \\ , radice \\ CIMV2 e \\ sottoscrizione radice all'avvio del sistema e preinstalla un set predefinito di definizioni di classe, incluse le [classi Win32](/windows/desktop/CIMWin32Prov/win32-provider), le [classi di sistema WMI](wmi-system-classes.md)e altre. Gli spazi dei nomi rimanenti presenti nel sistema vengono creati dai provider per altre parti del sistema operativo o dei prodotti. Per ulteriori informazioni e per un elenco di provider WMI disponibili nella maggior parte delle versioni del sistema operativo, vedere [provider WMI](wmi-providers.md).

    Il servizio WMI funge da intermediario tra i provider, le applicazioni di gestione e il repository WMI. Solo i dati statici sugli oggetti vengono archiviati nel repository, ad esempio le classi definite dai provider. WMI ottiene la maggior parte dei dati dinamicamente dal provider quando viene richiesto da un client. È anche possibile impostare le sottoscrizioni per ricevere notifiche degli eventi da un provider. Per ulteriori informazioni, vedere [monitoraggio degli eventi](monitoring-events.md).

-   Consumer WMI

    Un consumer WMI è un'applicazione di gestione o uno script che interagisce con l'infrastruttura WMI. Un'applicazione di gestione può eseguire query, enumerare dati, eseguire metodi del provider o sottoscrivere eventi chiamando l' [API com per WMI](com-api-for-wmi.md) o l' [API di scripting per WMI](scripting-api-for-wmi.md). Gli unici dati o azioni disponibili per un oggetto gestito, ad esempio un'unità disco o un servizio, sono quelli forniti da un provider.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di WMI](using-wmi.md)
</dt> <dt>

[Provider WMI](wmi-providers.md)
</dt> <dt>

[Creazione di un'applicazione o di uno script WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Attività WMI per script e applicazioni](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Invio di dati a WMI](providing-data-to-wmi.md)
</dt> <dt>

[Classi WMI](wmi-classes.md)
</dt> <dt>

[Monitoraggio degli eventi](monitoring-events.md)
</dt> <dt>

[Chiamata a un metodo](calling-a-method.md)
</dt> </dl>

 

 
