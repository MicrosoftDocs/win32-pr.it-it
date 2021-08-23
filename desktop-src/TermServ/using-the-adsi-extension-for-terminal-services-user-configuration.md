---
title: Uso dell'estensione ADSI per Servizi Desktop remoto utente
description: L'amministrazione delle proprietà utente specifiche di Servizi Desktop remoto è possibile usando i metodi implementati dall'estensione ADSI (Active Directory Service Interfaces), in pacchetto con la libreria a collegamento dinamico Tsuserex.dll.
ms.assetid: f6355730-9686-4446-b118-630562548fc9
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Servizi Desktop remoto , usando l'estensione ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe63a725531c21b64ed0ac10abdeb4f710465532ab95f7c416c88f6142f1d55e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119423691"
---
# <a name="using-the-adsi-extension-for-remote-desktop-services-user-configuration"></a>Uso dell'estensione ADSI per Servizi Desktop remoto utente

L'estensione ADSI (Active Directory Service Interfaces) per Servizi Desktop remoto configurazione utente è una libreria in pacchetto con la libreria a collegamento dinamico Tsuserex.dll. L'amministrazione Servizi Desktop remoto proprietà utente specifiche dell'utente è possibile usando i metodi implementati dall'estensione. I metodi consentono la configurazione delle proprietà disponibili nell'interfaccia di estensione per Servizi Desktop remoto utenti.

L'estensione ADSI Servizi Desktop remoto configurazione utente supporta l'esame e la manipolazione Servizi Desktop remoto proprietà utente archiviate nel database del servizio directory. L'estensione supporta anche la configurazione delle proprietà utente archiviate in Active Directory tramite l'API Lightweight Directory Access Protocol (LDAP).

Il provider implementa i metodi seguenti:

-   [**IADs::Get**](/windows/desktop/api/iads/nf-iads-iads-get). Questo metodo cerca una proprietà o un set di proprietà specifico in un'istanza della classe .
-   [**IADs::P ut**](/windows/desktop/api/iads/nf-iads-iads-put). Questo metodo configura una proprietà o un set di proprietà specifico in un'istanza della classe .

Per un elenco delle specifiche Servizi Desktop remoto utente che è possibile configurare, vedere Informazioni di riferimento per l'estensione [ADSI](reference-for-the-adsi-extension-for-terminal-services-user-configuration.md) per Servizi Desktop remoto'utente.

Per altre informazioni sull'accesso e la modifica degli attributi con ADSI, vedere Accesso e modifica dei dati [con ADSI.](/windows/desktop/ADSI/accessing-and-manipulating-data-with-adsi)

Per altre informazioni sull'uso delle convenzioni di denominazione [ADSI](/windows/desktop/ADSI/adsi-system-providers) e delle stringhe AdsPath, vedere le informazioni sui singoli provider di servizi ADSI nella documentazione di [Active Directory Service Interfaces](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) Platform Software Development Kit (SDK).

 

 