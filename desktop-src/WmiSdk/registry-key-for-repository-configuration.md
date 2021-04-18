---
description: Strumentazione gestione Windows (WMI) dispone di una nuova chiave del registro di sistema per abilitare o disabilitare la funzionalità di repository di autoripristino.
ms.assetid: 6c93fc40-b5d8-42da-9d02-7fa04fce3f65
ms.tgt_platform: multiple
title: Chiave del registro di sistema per la configurazione del repository
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed981da7c0540378746c78fecceefab8fc62559b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309911"
---
# <a name="registry-key-for-repository-configuration"></a>Chiave del registro di sistema per la configurazione del repository

Strumentazione gestione Windows (WMI) include una nuova chiave del registro di sistema per abilitare o disabilitare la funzionalità di repository di ripristino. Per ulteriori informazioni sul ripristino del repository WMI, vedere [backup o ripristino del repository WMI](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731460(v=ws.11)).

In Windows 7 il comportamento predefinito prevede il ripristino automatico di un repository da una versione di cui è stato eseguito il backup se viene rilevato un danneggiamento del repository. WMI fornisce il valore del registro di sistema **AutoRestoreEnabled** per disabilitare questa funzionalità.

Le chiavi del registro di sistema per WMI si trovano nel registro di sistema **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ .

<dl> <dt>

<span id="AutoRestoreEnabled"></span><span id="autorestoreenabled"></span><span id="AUTORESTOREENABLED"></span>**AutoRestoreEnabled**
</dt> <dd>

Consente all'utente di determinare se usare o meno la funzionalità di repository di autoripristino. Per impostazione predefinita, questa chiave è impostata su 1 e la funzionalità del repository autorestore è abilitata.

Sono possibili le impostazioni seguenti:

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

Disabled

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

Abilitato

</dd> </dl> </dd> </dl>

Il valore del registro di sistema **AutoRestoreEnabled** può essere modificato tramite il console Gestione criteri di gruppo (GPMC). Per ulteriori informazioni, vedere [console Gestione criteri di gruppo](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).

Questa procedura fornisce informazioni dettagliate su come abilitare o disabilitare la funzionalità di repository di autoripristino:

**Per modificare il valore predefinito della chiave **AutoRestoreEnabled** usando criteri di gruppo**

1.  Aprire Console Gestione Criteri di gruppo (GPMC).
2.  Creare un oggetto Criteri di gruppo (GPO).
3.  Modificare l'oggetto Criteri di gruppo.
4.  Passare a Preferenze/impostazioni di Windows/Registro di sistema.
5.  Fare clic con il pulsante destro del mouse e scegliere **nuovo... Registro di sistema**. Questa azione presenta un'interfaccia utente in cui è possibile immettere le informazioni del registro di sistema.
6.  Selezionare il comando **Aggiorna** .
7.  Selezionare il percorso della chiave del registro di sistema seguente: **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ WBEM \\ CIMOM**.
8.  Nel campo **nome** immettere **AutoRestoreEnabled**.
9.  Nel campo **dati** immettere 0 per disabilitare o 1 per abilitare la funzionalità di repository di ripristino di autoripristino.
10. Fare clic su OK.

 

 
