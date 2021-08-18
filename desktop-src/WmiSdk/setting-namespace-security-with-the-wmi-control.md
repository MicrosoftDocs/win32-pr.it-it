---
description: Il controllo WMI è uno snap-in MMC che si trova nel Pannello di controllo e viene utilizzato per impostare manualmente la sicurezza dello spazio dei nomi WMI in un computer locale. È anche possibile impostare lo spazio dei nomi predefinito per lo scripting.
ms.assetid: 87c23919-c482-4278-b005-894a8ac21da4
ms.tgt_platform: multiple
title: Impostazione della sicurezza dello spazio dei nomi con il controllo WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f97971e09897f8fa744f72d5ad0da59dc2292ebe7ceb88f6500e3c30e124db0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992351"
---
# <a name="setting-namespace-security-with-the-wmi-control"></a>Impostazione della sicurezza dello spazio dei nomi con il controllo WMI

Il controllo WMI è uno snap-in MMC che si trova nel **Pannello di controllo** e viene utilizzato per impostare manualmente la sicurezza dello spazio dei nomi WMI in un computer locale. È anche possibile impostare lo spazio dei nomi predefinito per lo scripting.


Nella procedura seguente viene descritto come individuare il controllo WMI.

**Per individuare il controllo WMI**

1.  Nella finestra **Pannello di controllo** fare doppio clic su **Strumenti di amministrazione**.
2.  Nella finestra **Strumenti di amministrazione** fare doppio clic su **Gestione computer**.
3.  Nella finestra **Gestione computer espandere** l'albero Servizi **e** applicazioni e fare doppio clic sul **controllo WMI**.
4.  Fare clic con il pulsante destro **del mouse sull'icona Controllo WMI** e scegliere **Proprietà.**

Nella procedura seguente viene descritto come utilizzare il controllo WMI per configurare la sicurezza per uno spazio dei nomi come modello, quindi ottenere a livello di codice le impostazioni di sicurezza per impostare la sicurezza per altri spazi dei nomi.

**Per impostare la sicurezza dello spazio dei nomi con il controllo WMI**

1.  Creare un nuovo spazio dei nomi usando Managed Object Format (MOF).
2.  Eseguire il controllo WMI per impostare la sicurezza nel nuovo spazio dei nomi. Nel menu **Start** fare clic su **Esegui** e digitare **wmimgmt.msc** oppure vedere [Individuazione del controllo WMI](#).
3.  Nel riquadro **Controllo WMI fare** clic con il pulsante destro del mouse su Controllo **WMI**, scegliere **Proprietà** e quindi selezionare la **scheda** Sicurezza .
4.  Passare al nuovo spazio dei nomi, fare clic **su Sicurezza** e quindi configurare gruppi e autorizzazioni per lo spazio dei nomi.

È anche possibile usare Windows Management Instrumentation Command-Line ([WMIC](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754534(v=ws.11))) per impostare la sicurezza dello spazio dei nomi. Per altre informazioni, vedere [**wmic.**](wmic.md)

## <a name="setting-the-default-namespace-for-scripts"></a>Impostazione dello spazio dei nomi predefinito per gli script

Se uno script non si connette in modo esplicito a uno spazio dei nomi durante la connessione a WMI, WMI usa lo spazio dei nomi predefinito specificato in questo controllo. Il valore predefinito si trova anche nella voce del Registro di sistema come indicato di seguito:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         WBEM
            Scripting
               Default
                  Namespace
```

Poiché lo spazio dei nomi predefinito è facile da modificare, con questo controllo o a livello di codice chiamando i metodi di [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), specificare lo spazio dei nomi durante la connessione a WMI tramite [il moniker](constructing-a-moniker-string.md) o le chiamate a [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md). Per altre informazioni, vedere [Creazione di uno script WMI](creating-a-wmi-script.md)

**Per impostare lo spazio dei nomi predefinito per gli script**

1.  Nella finestra **Proprietà controllo WMI** scegliere la **scheda** Avanzate.
2.  Fare clic **sul pulsante** Cambia e selezionare lo spazio dei nomi per impostare l'impostazione predefinita.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione dei descrittori di sicurezza dello spazio dei nomi](setting-namespace-security-descriptors.md)
</dt> </dl>

 

 
