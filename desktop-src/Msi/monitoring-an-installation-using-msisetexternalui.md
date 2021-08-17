---
description: Gli autori di pacchetti possono monitorare i messaggi interni Windows Installer tramite la creazione di un'applicazione eseguibile che contiene un gestore di callback per ricevere i messaggi e le funzionalità per avviare un'installazione.
ms.assetid: 0aa8a2d6-f519-4d87-a28f-a11cb546bff5
title: Monitoraggio di un'installazione tramite MsiSetExternalUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9660b1454d7e4f3437da6dce41707a1516207d853510e8475837f31e60090b78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628572"
---
# <a name="monitoring-an-installation-using-msisetexternalui"></a>Monitoraggio di un'installazione tramite MsiSetExternalUI

Gli autori di pacchetti possono monitorare i messaggi interni Windows Installer tramite la creazione di un'applicazione eseguibile che contiene un gestore di callback per ricevere i messaggi e le funzionalità per avviare un'installazione.

Il gestore di callback è conforme al prototipo INSTALLUI HANDLER e un puntatore a questo gestore di callback viene \_ passato [**a MsiSetExternalUI.**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) Dopo che l'installazione è stata avviata da una chiamata a [**MsiInstallProduct,**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)i messaggi di installazione vengono intercettati dal gestore di callback e l'autore del pacchetto può visualizzare o ignorare in modo selettivo uno o tutti questi messaggi.

Per altre informazioni, vedere Gestione dei messaggi di stato tramite [MsiSetExternalUI,](handling-progress-messages-using-msisetexternalui.md)Restituzione di valori da un gestore [di Interfaccia utente](returning-values-from-an-external-user-interface-handler.md)esterno e Analisi dei messaggi Windows programma [di installazione.](parsing-windows-installer-messages.md)

Per altre informazioni sull'uso di un gestore esterno basato su record, vedere Monitoraggio di un'installazione [tramite MsiSetExternalUIRecord.](monitoring-an-installation-using-msisetexternaluirecord.md)

 

 



