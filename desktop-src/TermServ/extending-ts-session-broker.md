---
title: Estensione di Gestore sessione Servizi terminal
description: È possibile estendere TS \ 160; Gestore di sessione tramite l'interfaccia COM IWTSSBPlugin.
ms.assetid: f111d6e6-90ca-4eff-ab0e-02de25f7d6ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c859320c11a128ab01a719d17abd9927ea96f312e0aa3df5f0be76dcc0226b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737691"
---
# <a name="extending-terminal-services-session-broker"></a>Estensione di Gestore sessione Servizi terminal

Gestore di sessione Servizi terminal determina se un utente che avvia una connessione ha già una sessione aperta. In questo caso, Gestore sessione Servizi terminal instrada la connessione in ingresso al server host sessione Desktop remoto (Host sessione Desktop remoto) con la sessione esistente. In caso contrario, Gestore sessione Servizi terminal instrada la connessione in ingresso al server Host sessione Desktop remoto con il numero minimo di sessioni.

È possibile estendere TS Session Broker usando [**l'interfaccia COM IWTSSBPlugin.**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) È possibile usare questa interfaccia per gestire le connessioni ai server Host sessione Desktop remoto, nonché qualsiasi tipo di connessione Remote Desktop Protocol (RDP), ad esempio le connessioni alle macchine virtuali guest che eseguono Windows Vista Enterprise Centraled Desktop (VECD) in un host macchina virtuale Hyper-V di Windows Server 2008.

[**L'interfaccia IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) offre diversi vantaggi:

-   Non è necessario installare un agente nel client o nel server Host sessione Desktop remoto.
-   Il plug-in può interagire senza problemi con altri servizi ruolo Servizi Desktop remoto, ad esempio gateway Desktop remoto e basarsi sulle informazioni di Gestore sessione Servizi terminal sugli stati della sessione e del computer.
-   È possibile usare il plug-in per gestire le connessioni con dispositivi client o server che supportano RDP 5.2 o versione successiva.
-   È possibile usare il plug-in per abilitare Windows Vista Enterprise soluzioni desktop centralizzate.

Quando si implementano i metodi di questa interfaccia, tenere presente quanto segue:

-   TS Session Broker potrebbe chiamare i metodi di questo oggetto COM da più thread.
-   Se uno dei metodi chiamati non restituisce immediatamente e correttamente, TS Session Broker non effettua più chiamate al plug-in e ripristina la logica di bilanciamento del carico nativa. Per riprendere le chiamate al plug-in, è necessario riavviare il servizio Gestore sessione Servizi terminal.
-   È necessario registrare il plug-in come oggetto COM a livello di sistema usando Regsvr32.exe. Poiché il servizio Gestore sessione Servizi terminal viene eseguito con l'account "NetworkService", è necessario assegnare all'account "NetworkService" le autorizzazioni di avvio, attivazione e accesso necessarie usando Dcomcnfg.exe. Il servizio Gestore sessione Servizi terminal cerca il CLSID dell'oggetto COM che rappresenta il plug-in nella sottochiave del Registro di sistema seguente:

    **HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **Tssdis** \\ **Parameters** \\ **ExtensibilityPluginCLSID**

Per altre informazioni sui Dcomcnfg.exe, vedere [Abilitazione della sicurezza COM tramite DCOMCNFG.](/windows/desktop/com/enabling-com-security-using-dcomcnfg)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> </dl>

 

 