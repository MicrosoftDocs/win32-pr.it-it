---
title: Uso dell'estensione ADSI per la configurazione di Servizi Desktop remoto utente
description: L'amministrazione delle proprietà utente specifiche di Servizi Desktop remoto è possibile utilizzando i metodi implementati dall'estensione ADSI (Active Directory Service Interfaces), assemblata con la libreria a collegamento dinamico Tsuserex.dll.
ms.assetid: f6355730-9686-4446-b118-630562548fc9
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Servizi Desktop remoto utilizzando l'estensione ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f115fecf1cce5c518e93206402f76e077109611
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963388"
---
# <a name="using-the-adsi-extension-for-remote-desktop-services-user-configuration"></a>Uso dell'estensione ADSI per la configurazione di Servizi Desktop remoto utente

L'estensione ADSI (Active Directory Service Interfaces) per la configurazione dell'utente Servizi Desktop remoto è una raccolta di pacchetti con la libreria a collegamento dinamico Tsuserex.dll. L'amministrazione delle proprietà utente specifiche di Servizi Desktop remoto è possibile utilizzando i metodi implementati dall'estensione. I metodi consentono la configurazione delle proprietà disponibili nell'interfaccia di estensione per Servizi Desktop remoto utenti.

L'estensione ADSI per Servizi Desktop remoto Configurazione utente supporta l'analisi e la manipolazione delle proprietà Servizi Desktop remoto utente archiviate nel database del servizio directory. L'estensione supporta inoltre la configurazione di proprietà utente archiviate nel Active Directory tramite l'API LDAP (Lightweight Directory Access Protocol).

Il provider implementa i metodi seguenti:

-   [**IADs:: Get**](/windows/desktop/api/iads/nf-iads-iads-get). Questo metodo cerca una proprietà o un set di proprietà specifico in un'istanza della classe.
-   [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put). Questo metodo configura una proprietà o un set di proprietà specifico in un'istanza della classe.

Per un elenco delle proprietà utente Servizi Desktop remoto specifiche che è possibile configurare, vedere la Guida di [riferimento per l'estensione ADSI per Servizi Desktop remoto Configurazione utente](reference-for-the-adsi-extension-for-terminal-services-user-configuration.md) .

Per ulteriori informazioni sull'accesso e la modifica degli attributi con ADSI, vedere [accesso e modifica di dati con ADSI](/windows/desktop/ADSI/accessing-and-manipulating-data-with-adsi).

Per ulteriori informazioni sull'utilizzo delle convenzioni di denominazione ADSI e delle stringhe AdsPath, vedere le informazioni sui singoli [provider di servizi ADSI](/windows/desktop/ADSI/adsi-system-providers) nella documentazione di [Active Directory Service Interfaces](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) Platform SDK (SDK).

 

 