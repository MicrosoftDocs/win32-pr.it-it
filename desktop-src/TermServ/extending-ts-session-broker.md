---
title: Estensione di broker di sessione di Servizi terminal
description: È possibile estendere TS \ 160; Broker di sessione mediante l'interfaccia COM IWTSSBPlugin.
ms.assetid: f111d6e6-90ca-4eff-ab0e-02de25f7d6ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b84471bcf2125017b8eef273cdb78e61a9bc620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729290"
---
# <a name="extending-terminal-services-session-broker"></a>Estensione di broker di sessione di Servizi terminal

Gestore sessioni Servizi terminal determina se un utente che avvia una connessione dispone già di una sessione aperta. In tal caso, broker di sessione di Servizi terminal instrada la connessione in ingresso al server host sessione Desktop remoto (host sessione Desktop remoto) con la sessione esistente. In caso contrario, broker di sessione di Servizi terminal instrada la connessione in ingresso al server Host sessione Desktop remoto con il minor numero di sessioni.

È possibile estendere broker di sessione di Servizi terminal tramite l'interfaccia com [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) . È possibile utilizzare questa interfaccia per gestire le connessioni ai server Host sessione Desktop remoto e a qualsiasi tipo di connessione di Remote Desktop Protocol (RDP), ad esempio, le connessioni alle macchine virtuali guest che eseguono Windows Vista Enterprise centralizzate desktop (VECD) in un host macchina virtuale Hyper-V di Windows Server 2008.

L'interfaccia [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) offre diversi vantaggi:

-   Non è necessario installare un agente nel client o nel server Host sessione Desktop remoto.
-   Il plug-in può interagire senza interruzioni con altri servizi ruolo Servizi Desktop remoto, ad esempio Desktop remoto Gateway (Gateway Desktop remoto) e basarsi sulle informazioni provenienti da broker di sessione di Servizi terminal sugli stati di sessione e computer.
-   È possibile usare il plug-in per gestire le connessioni con i dispositivi client o server che supportano RDP 5,2 o versione successiva.
-   È possibile utilizzare il plug-in per abilitare le soluzioni desktop centralizzate di Windows Vista Enterprise.

Quando si implementano i metodi di questa interfaccia, tenere presenti i seguenti aspetti:

-   Broker di sessione di Servizi terminal può chiamare i metodi di questo oggetto COM da più thread.
-   Se uno dei metodi chiamati non viene restituito immediatamente e correttamente, broker di sessione di Servizi terminal non effettua più chiamate al plug-in e ripristina la logica di bilanciamento del carico nativa. Per riprendere le chiamate al plug-in, è necessario riavviare il servizio Gestore sessioni Servizi terminal.
-   È necessario registrare il plug-in come oggetto COM a livello di sistema utilizzando Regsvr32.exe. Poiché il servizio Gestore sessioni Servizi terminal viene eseguito con l'account "NetworkService", è necessario assegnare all'account "NetworkService" le autorizzazioni di avvio, attivazione e accesso richieste usando Dcomcnfg.exe. Il servizio Gestore sessioni Servizi terminal Cerca il CLSID dell'oggetto COM che rappresenta il plug-in nella seguente sottochiave del registro di sistema:

    **HKEY \_ \_Computer locale** \\ **sistema** \\ **CurrentControlSet** \\ **Servizi** \\ **Tssdis** \\ **parametri** \\ **ExtensibilityPluginCLSID**

Per ulteriori informazioni su Dcomcnfg.exe, vedere [Abilitazione della sicurezza com tramite DCOMCNFG](/windows/desktop/com/enabling-com-security-using-dcomcnfg).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> </dl>

 

 