---
title: Autenticazione (Servizi di dominio Active Directory)
description: Ogni oggetto in Active Directory Domain Services ha un descrittore di sicurezza univoco che definisce le autorizzazioni di accesso necessarie per leggere o aggiornare l'oggetto o le relative singole proprietà.
ms.assetid: a4a663d3-b0f3-4993-a74e-9e4f896e8c95
ms.tgt_platform: multiple
keywords:
- Active Directory, uso, associazione, autenticazione
- associazione dell'autenticazione ad Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87eb07e05b9f817d894c13d089cf9ec1291ca14b58b640c9a4c26ae9cff8c44d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024222"
---
# <a name="authentication-ad-ds"></a>Autenticazione (Servizi di dominio Active Directory)

Ogni oggetto in Active Directory Domain Services ha un descrittore di sicurezza univoco che definisce le autorizzazioni di accesso necessarie per leggere o aggiornare l'oggetto o le relative singole proprietà. I privilegi di accesso sono determinati dai diritti concessi all'account o all'appartenenza a gruppi di un utente.

Quando un'applicazione viene associata a un oggetto nella directory, i privilegi di accesso dell'applicazione a tale oggetto si basano sul contesto utente specificato durante l'operazione di associazione. Per le funzioni e i metodi di associazione [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject), [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject), **GetObject**, [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject), un'applicazione può usare in modo implicito le credenziali del chiamante, specificare in modo esplicito le credenziali di un account utente o usare un contesto utente non autenticato (Guest).

 

 