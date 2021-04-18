---
title: Blocco account (provider LDAP)
description: Quando viene superato il numero di tentativi di accesso non riusciti, l'account utente viene bloccato per un periodo di tempo specificato dall'attributo lockoutDuration.
ms.assetid: bf86f6ac-8209-4306-8736-99ce53c93617
ms.tgt_platform: multiple
keywords:
- Blocco account (provider LDAP) ADSI
- Blocco account ADSI, provider LDAP
- Provider LDAP ADSI, esempi di gestione degli utenti, blocco degli account
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697b7a25943debfd08469ce9a28463c88159ded9
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300450"
---
# <a name="account-lockout-ldap-provider"></a>Blocco account (provider LDAP)

Quando viene superato il numero di tentativi di accesso non riusciti, l'account utente viene bloccato per un periodo di tempo specificato dall'attributo [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) . La proprietà [**IADsUser. IsAccountLocked**](iadsuser-property-methods.md) sembra essere la proprietà da usare per leggere e modificare lo stato di blocco di un account utente, ma il provider ADSI LDAP non supporta accuratamente la proprietà **IsAccountLocked** . Per ottenere e impostare dati di blocco degli account accurati, utilizzare il provider WinNT. Per ulteriori informazioni sull'utilizzo della proprietà **IsAccountLocked** con il provider WinNT, vedere [blocco account (provider WinNT)](winnt-account-lockout.md).

 

 