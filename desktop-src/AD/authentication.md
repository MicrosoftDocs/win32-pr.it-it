---
title: Autenticazione (AD DS)
description: Ogni oggetto in Active Directory Domain Services dispone di un descrittore di sicurezza univoco che definisce le autorizzazioni di accesso necessarie per leggere o aggiornare l'oggetto o le sue singole proprietà.
ms.assetid: a4a663d3-b0f3-4993-a74e-9e4f896e8c95
ms.tgt_platform: multiple
keywords:
- Active Directory, utilizzo, associazione, autenticazione
- Binding autenticazione AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb80bbca4604a99011d3198eaf6b3e871cd3f84c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472699"
---
# <a name="authentication-ad-ds"></a>Autenticazione (AD DS)

Ogni oggetto in Active Directory Domain Services dispone di un descrittore di sicurezza univoco che definisce le autorizzazioni di accesso necessarie per leggere o aggiornare l'oggetto o le sue singole proprietà. I privilegi di accesso sono determinati dai diritti concessi per l'appartenenza a un account utente o a un gruppo.

Quando un'applicazione viene associata a un oggetto nella directory, i privilegi di accesso dell'applicazione a tale oggetto sono basati sul contesto utente specificato durante l'operazione di associazione. Per le funzioni e i metodi di associazione [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject), [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject), **GetObject**, [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject), un'applicazione può usare in modo implicito le credenziali del chiamante, specificare in modo esplicito le credenziali di un account utente oppure usare un contesto utente non autenticato (Guest).

 

 