---
description: Contiene informazioni sull'interfaccia di programmazione per il servizio Wireless Zero Configuration in Windows XP e Windows Server 2003.
ms.assetid: cd9e8fc0-0a65-4654-95aa-201751183521
title: Informazioni di riferimento su Wireless Zero Configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 358ff3727edc34d4a5de0f4195895cf02b4596722aecd5849f4e35b9991dbe88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684431"
---
# <a name="wireless-zero-configuration-reference"></a>Informazioni di riferimento su Wireless Zero Configuration

\[L'interfaccia di programmazione Wireless Zero Configuration non è più supportata a Windows Vista e Windows Server 2008. Usare invece [l'API Wi-Fi nativa](native-wifi-reference.md), che offre funzionalità simili. Per altre informazioni, vedere [Informazioni sull'API Wi-Fi nativa.](about-the-native-wifi-api.md)\]

Questa sezione contiene informazioni sull'interfaccia di programmazione per il servizio Wireless Zero Configuration in Windows XP e Windows Server 2003. Gli argomenti includono:

-   [Funzioni wireless zero configuration](wireless-zero-configuration-functions.md)
-   [Strutture di configurazione wireless zero](wireless-zero-configuration-structures.md)

Wireless Zero Configuration è un servizio Windows in Windows XP e Windows Server 2003 che viene utilizzato per configurare e gestire le connessioni di rete wireless su una scheda wireless. Il nome del servizio per Wireless Zero Configuration è WZCSVC. In Windows XP il nome visualizzato per il servizio WZCSVC è Wireless Zero Configuration. In Windows Server 2003, il nome visualizzato per il servizio WZCSVC è Configurazione wireless.

Il servizio Wireless Zero Configuration viene in genere avviato in fase di avvio. L'interfaccia di programmazione per il servizio Wireless Zero Configuration può essere utilizzata solo se il servizio Wireless Zero Configuration è stato avviato. Se il servizio Wireless Zero Configuration non viene avviato, le funzioni Wireless Zero Configuration restituirà un errore.

Per abilitare il servizio Wireless Zero Configuration in modo che si avvia automaticamente, passare al **pulsante** Start. Selezionare **l Impostazioni** e quindi selezionare **Pannello di controllo**. Se si usa la visualizzazione Windows XP, selezionare **la** categoria Prestazioni e manutenzione e quindi Strumenti **di amministrazione**. Se si usa la visualizzazione classica, selezionare Strumenti **di amministrazione**. Fare clic **sull'icona** Servizi nel riquadro sinistro. Fare clic sull'icona Wireless Zero Configuration (Configurazione zero wireless) nel riquadro destro e impostare la casella di **controllo Tipo di avvio** su **Automatico.** Questa impostazione imposta l'avvio automatico del servizio in fase di avvio. Fare quindi clic **sul pulsante Start** per avviare il servizio Wireless Zero Wireless Zero Configuration e fare clic sul pulsante **OK.**

Wireless Zero Configuration può anche essere avviato e arrestato da un prompt dei comandi. Per avviare Wireless Zero Configuration, eseguire il comando seguente:

**net start wzcsvc**

Per arrestare Wireless Zero Configuration, eseguire il comando seguente:

**net stop wzcsvc**

 

 



