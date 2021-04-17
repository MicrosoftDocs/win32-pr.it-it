---
title: Fornire le autorizzazioni utente per i dispositivi con masterizzazione multimediale
description: Per impostazione predefinita, Windows Vista e Windows Server 2008 concedono l'accesso in lettura/scrittura agli amministratori e agli utenti connessi direttamente al computer (utenti intermedi).
ms.assetid: 5bb8c8fc-03b4-45b5-816c-45f6cd580de6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613eb1bba9a18cfb08e1eee3e6b86c34235ab8e9
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "104234423"
---
# <a name="providing-user-permissions-for-media-burning-devices"></a>Fornire le autorizzazioni utente per i dispositivi con masterizzazione multimediale

Per impostazione predefinita, Windows Vista e Windows Server 2008 concedono l'accesso in lettura/scrittura agli amministratori e agli utenti connessi direttamente al computer (utenti intermedi). Tuttavia, in Windows XP e Windows Server 2003 un amministratore deve concedere questi privilegi di lettura/scrittura al dispositivo ad altri gruppi di utenti.

Un amministratore può modificare le autorizzazioni specifiche relative ai dispositivi per utenti esperti e utenti interattivi.

Per accedere al pannello autorizzazioni gruppo appropriato in Windows XP, fare clic sul pulsante **Start**, scegliere **Esegui**, digitare **gpedit. msc**, quindi fare clic su **OK**. Nell'interfaccia Criteri di gruppo espandere **Configurazione computer**, **impostazioni di Windows**, **Impostazioni protezione**, **criteri locali**, quindi fare doppio clic su **Opzioni di sicurezza**.

![Screenshot che mostra la finestra "Criteri di gruppo" con i criteri selezionati nel riquadro "criteri".](images/gpolpanel.jpg)

In questo pannello, un amministratore deve specificare le impostazioni di due opzioni del dispositivo per fornire le autorizzazioni necessarie per il gruppo:

-   Imposta "dispositivi: limita l'accesso CD-ROM al solo utente connesso localmente" per **abilitare**
-   Impostare "dispositivi: consentito formattare ed estrarre supporti rimovibili" per **gli amministratori e gli utenti avanzati**. È inoltre possibile emulare le autorizzazioni di Windows Vista impostando questa opzione su **amministratori e utenti interattivi**.

Sebbene non esista un'interfaccia utente specifica in Windows XP o Windows Server 2003 per l'uso di [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) o [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya), è possibile usare queste API per concedere a gruppi di utenti personalizzati le autorizzazioni per i dispositivi. Una chiamata a **SetSecurityInfo** , ad esempio, consentirà di concedere le autorizzazioni ai gruppi di utenti. Le modifiche alle autorizzazioni con questa API sono temporanee e non verranno mantenute durante il riavvio. Tuttavia, la chiamata di [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya) implementerà le modifiche delle autorizzazioni nel registro di sistema, che rimarranno in modo permanente in un riavvio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di IMAPi](using-imapi.md)
</dt> <dt>

[**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)
</dt> <dt>

[SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya)
</dt> </dl>

 

 