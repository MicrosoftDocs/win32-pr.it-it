---
description: WMI offre un'interfaccia uniforme per applicazioni o script locali o remoti che ottengono dati di gestione da un sistema informatico, una rete o un'azienda.
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
ms.openlocfilehash: e261459785fa4e0ccdce7337df788de007c6f335799bbe4778e80f551f5e519e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995526"
---
# <a name="wmi-architecture"></a>Architettura WMI

WMI offre un'interfaccia uniforme per applicazioni o script locali o remoti che ottengono dati di gestione da un sistema informatico, una rete o un'azienda. L'interfaccia uniforme è progettata in modo che gli script e le applicazioni client WMI non devono chiamare un'ampia gamma di API (Application Programming Interface) del sistema operativo. Molte API non possono essere chiamate da client di automazione come script o Visual Basic applicazioni. Altre API non effettuano chiamate a computer remoti.

Per ottenere dati da WMI, scrivere uno script client o un'applicazione che accede alle classi [WMI](wmi-classes.md) o fornisce dati a WMI scrivendo un [*provider WMI.*](gloss-p.md) Per altre informazioni, vedere [Uso di WMI.](using-wmi.md)

## <a name="objects-consumers-and-infrastructure-of-wmi"></a>Oggetti, consumer e infrastruttura di WMI

Il diagramma seguente illustra la relazione tra l'infrastruttura WMI e i provider WMI e gli oggetti gestiti e mostra anche la relazione tra l'infrastruttura WMI e i consumer WMI.

![relazione tra l'infrastruttura WMI, i provider WMI e gli oggetti gestiti](images/wmi-architecture.png)

## <a name="wmi-components"></a>Componenti WMI

L'elenco seguente descrive i componenti WMI principali:

-   Oggetti gestiti e provider WMI

    Un provider WMI è un oggetto COM che monitora uno o più [*oggetti gestiti*](gloss-m.md) per WMI. Un oggetto gestito è un componente aziendale logico o fisico, ad esempio un disco rigido, una scheda di rete, un sistema di database, un sistema operativo, un processo o un servizio.

    Analogamente a un driver, un provider fornisce a WMI i dati di un oggetto gestito e gestisce i messaggi da WMI all'oggetto gestito. I provider WMI sono costituiti da un file DLL e da un file [*MOF (Managed Object Format)*](gloss-m.md) che definisce le classi per cui il provider restituisce dati ed esegue operazioni. I provider, ad esempio le applicazioni WMI C++, usano [l'API COM per WMI.](com-api-for-wmi.md) Per altre informazioni, vedere [Fornire dati a WMI.](providing-data-to-wmi.md)

    Un esempio di provider è il [provider](/previous-versions/windows/desktop/regprov/system-registry-provider)del Registro di sistema preinstallato , che accede ai dati nel Registro di sistema. Il provider del Registro di sistema ha una classe [*WMI,*](gloss-w.md) [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), con molti metodi ma nessuna proprietà. Altri provider preinstallati, ad esempio il [provider Win32](/windows/desktop/CIMWin32Prov/win32-provider), in genere dispongono di classi con molte proprietà ma con pochi metodi, ad esempio [**processo \_ Win32**](/windows/desktop/CIMWin32Prov/win32-process) o [**\_ LogicalDisk Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) Il file DLL del provider del Registro di sistema, Stdprov.dll, contiene il codice che restituisce dinamicamente i dati quando richiesto da script client o applicazioni.

    I file MOF e DLL WMI si trovano in %WINDIR% \\ System32 \\ Wbem, [](winmgmt.md) [****](mofcomp.md)insieme agli strumenti [Command-Line WMI](wmi-command-line-tools.md), ad esempioWinmgmt.exeeMofcomp.exe. Le classi provider, ad esempio [**\_ LogicalDisk Win32,**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)vengono definite nei file MOF e quindi compilate nel repository WMI all'avvio del sistema.

-   [Infrastruttura WMI](wmi-infrastructure.md)

    L'infrastruttura WMI è un componente Windows del sistema operativo di Microsoft, che è il servizio WMI (winmgmt). L'infrastruttura WMI ha due componenti: WMI Core e il [*repository WMI*](gloss-w.md).

    Il repository WMI è organizzato in base a spazi [*dei nomi WMI.*](gloss-n.md) Il servizio WMI crea alcuni spazi dei nomi, ad esempio root \\ default, root cimv2 e root subscription all'avvio del sistema e preinstalla un set predefinito di definizioni di classe, tra cui le \\ \\ classi [Win32](/windows/desktop/CIMWin32Prov/win32-provider), [](wmi-system-classes.md)le classi di sistema WMI e altri. Gli spazi dei nomi rimanenti presenti nel sistema vengono creati dai provider per altre parti del sistema operativo o dei prodotti. Per altre informazioni e un elenco dei provider WMI disponibili nella maggior parte delle versioni del sistema operativo, vedere [Provider WMI](wmi-providers.md).

    Il servizio WMI funge da intermediario tra i provider, le applicazioni di gestione e il repository WMI. Solo i dati statici sugli oggetti vengono archiviati nel repository, ad esempio le classi definite dai provider. WMI ottiene la maggior parte dei dati in modo dinamico dal provider quando un client lo richiede. È anche possibile configurare le sottoscrizioni per ricevere notifiche degli eventi da un provider. Per altre informazioni, vedere [Monitoraggio degli eventi](monitoring-events.md).

-   Consumer WMI

    Un consumer WMI è uno script o un'applicazione di gestione che interagisce con l'infrastruttura WMI. Un'applicazione di gestione può eseguire query, enumerare dati, eseguire metodi provider o sottoscrivere eventi chiamando [l'API COM](com-api-for-wmi.md) per WMI o l'API scripting [per WMI.](scripting-api-for-wmi.md) Gli unici dati o azioni disponibili per un oggetto gestito, ad esempio un'unità disco o un servizio, sono quelli forniti da un provider.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di WMI](using-wmi.md)
</dt> <dt>

[Provider WMI](wmi-providers.md)
</dt> <dt>

[Creazione di un'applicazione o di uno script WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Attività WMI per script e applicazioni](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Fornire dati a WMI](providing-data-to-wmi.md)
</dt> <dt>

[Classi WMI](wmi-classes.md)
</dt> <dt>

[Monitoraggio degli eventi](monitoring-events.md)
</dt> <dt>

[Chiamata di un metodo](calling-a-method.md)
</dt> </dl>

 

 
