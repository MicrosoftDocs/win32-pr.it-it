---
description: Contiene informazioni sull'interfaccia di programmazione per il servizio Wireless Zero Configuration in Windows XP e Windows Server 2003.
ms.assetid: cd9e8fc0-0a65-4654-95aa-201751183521
title: Riferimento alla configurazione senza fili zero
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebe202e16aa38fef617f382559f124772d50a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227390"
---
# <a name="wireless-zero-configuration-reference"></a>Riferimento alla configurazione senza fili zero

\[L'interfaccia di programmazione Wireless Zero Configuration non è più supportata a partire da Windows Vista e Windows Server 2008. Usare invece l' [API WiFi nativa](native-wifi-reference.md), che fornisce funzionalità simili. Per ulteriori informazioni, vedere [informazioni sull'API WiFi nativa](about-the-native-wifi-api.md).\]

Questa sezione contiene informazioni sull'interfaccia di programmazione per il servizio Wireless Zero Configuration in Windows XP e Windows Server 2003. Gli argomenti includono:

-   [Funzioni di configurazione senza fili zero](wireless-zero-configuration-functions.md)
-   [Strutture di configurazione senza fili zero](wireless-zero-configuration-structures.md)

La configurazione wireless zero è un servizio Windows in Windows XP e Windows Server 2003 utilizzato per configurare e gestire le connessioni di rete wireless in una scheda wireless. Il nome del servizio per la configurazione wireless zero è WZCSVC. In Windows XP, il nome visualizzato per il servizio WZCSVC è la configurazione wireless zero. In Windows Server 2003, il nome visualizzato per il servizio WZCSVC è configurazione wireless.

Il servizio di configurazione zero senza fili viene in genere avviato in fase di avvio. L'interfaccia di programmazione per il servizio di configurazione zero wireless può essere usata solo se il servizio di configurazione zero wireless è stato avviato. Se il servizio di configurazione zero senza fili non è avviato, le funzioni di configurazione zero wireless restituiranno un errore.

Per abilitare il servizio di configurazione zero wireless in modo che venga avviato automaticamente, passare al pulsante **Avvia** . Selezionare l'opzione **Impostazioni** e quindi selezionare **Pannello di controllo**. Se si utilizza la vista Windows XP, selezionare la categoria **prestazioni e manutenzione** , quindi selezionare **strumenti di amministrazione**. Se si usa la visualizzazione classica, scegliere Strumenti di **Amministrazione**. Fare clic sull'icona **Servizi** nel riquadro sinistro. Fare clic sull'icona configurazione wireless zero nel riquadro di destra e modificare il **tipo di avvio** Dropbox in **automatico**. Questa impostazione consente di impostare il servizio per l'avvio automatico in fase di avvio. Fare quindi clic sul pulsante **Start** per avviare il servizio Wireless Zero Wireless Zero Configuration e fare clic sul pulsante **OK** .

È anche possibile avviare e arrestare la configurazione wireless zero da un prompt dei comandi. Per avviare la configurazione wireless zero, eseguire il comando seguente:

**NET Start WZCSVC**

Per arrestare la configurazione wireless zero, eseguire il comando seguente:

**NET STOP WZCSVC**

 

 



