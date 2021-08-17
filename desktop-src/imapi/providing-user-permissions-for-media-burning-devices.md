---
title: Fornire le autorizzazioni utente per i dispositivi di media che esegnano contenuti multimediali
description: Per impostazione predefinita, Windows Vista e Windows Server 2008 concedono l'accesso in lettura/scrittura agli amministratori e agli utenti connessi direttamente al computer (utenti intermedi).
ms.assetid: 5bb8c8fc-03b4-45b5-816c-45f6cd580de6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1c5827b960405855ba34880e39750b39d4f934e395167479b7cae7912721af5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758563"
---
# <a name="providing-user-permissions-for-media-burning-devices"></a>Fornire le autorizzazioni utente per i dispositivi di media che esegnano contenuti multimediali

Per impostazione predefinita, Windows Vista e Windows Server 2008 concedono l'accesso in lettura/scrittura agli amministratori e agli utenti connessi direttamente al computer (utenti intermedi). Tuttavia, in Windows XP e Windows Server 2003 un amministratore deve concedere questi privilegi di lettura/scrittura del dispositivo ad altri gruppi di utenti.

Un amministratore può modificare autorizzazioni specifiche relative ai dispositivi per gli utenti esperti e gli utenti interattivi.

Per accedere al pannello delle autorizzazioni di gruppo appropriato in Windows XP, fare clic su **Start**, scegliere **Esegui**, digitare **gpedit.msc** e quindi fare clic su **OK.** Nell'interfaccia Criteri di gruppo computer espandere Configurazione computer **,** espandere **Windows Impostazioni**, Sicurezza **Impostazioni**, Criteri **localie** fare doppio clic su **Opzioni di sicurezza**.

![Screenshot che mostra la finestra "Criteri di gruppo" con un criterio selezionato nel riquadro "Criteri".](images/gpolpanel.jpg)

In questo pannello, un amministratore deve specificare le impostazioni di due opzioni del dispositivo per fornire le autorizzazioni di gruppo necessarie:

-   Impostare "Devices: Restrict CD-ROM access to locally logged on user only" (Dispositivi: Limita l'accesso cd-ROM solo all'utente connesso in locale) su **Enabled (Abilitato)**
-   Impostare "Devices: Allowed to format and eject removable media" (Dispositivi: è consentito formattare e rimuovere supporti rimovibili) **su Administrators e Power Users.** È anche possibile emulare le Windows Vista impostando questa opzione su **Amministratori e Utenti interattivi.**

Anche se non esiste un'interfaccia utente specifica in Windows XP o Windows Server 2003 per l'uso di [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) o [SetupDiSetDeviceRegistryProperty,](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya)è possibile usare queste API per concedere autorizzazioni per dispositivi ai gruppi di utenti personalizzati. Ad esempio, una chiamata a **SetSecurityInfo concederà** le autorizzazioni ai gruppi di utenti. Le modifiche alle autorizzazioni con questa API sono temporanee e non verranno mantenute durante un riavvio. Tuttavia, la chiamata [a SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya) implementerà le modifiche delle autorizzazioni nel Registro di sistema, che verranno mantenute dopo un riavvio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di IMAPI](using-imapi.md)
</dt> <dt>

[**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)
</dt> <dt>

[Proprietà SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya)
</dt> </dl>

 

 