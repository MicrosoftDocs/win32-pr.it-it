---
title: add urlacl
description: Riserva l'URL specificato per gli utenti e gli account non amministratori.
ms.assetid: 5d89dec3-26e6-4db8-b4cc-e9b933ac60c5
keywords:
- Aggiungi urlacl HTTP
topic_type:
- apiref
api_name:
- add urlacl
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: 16f6cb64c0c784f3a5400e2c97e212edbc50936c
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "103969289"
---
# <a name="add-urlacl"></a>add urlacl

Riserva l'URL specificato per gli utenti e gli account non amministratori. È possibile specificare l'elenco di controllo di accesso discrezionale (DACL) utilizzando un nome di account con i parametri Listen e Delegate oppure utilizzando una stringa SDDL (Security Descriptor Definition Language).

``` syntax
add urlacl [url=]string
           [[user=]string
           {[[listen={yes|no}] [delegate={yes|no}]] | [sddl=]string}

 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>
**[URL =] stringa**
</dt> <dd>

Specifica l'URL completo.

</dd> <dt>

<span id="_user__string"></span><span id="_USER__STRING"></span>
**stringa [user =]**
</dt> <dd>

Specifica il nome dell'utente o del gruppo di utenti.

</dd> <dt>

<span id="_listen__yes_no__"></span><span id="_LISTEN__YES_NO__"></span>**\[ascolto = {Sì \| No}\]**
</dt> <dd>

Specifica uno dei valori seguenti:

-   Sì: consente all'utente di registrare gli URL. Si tratta del valore predefinito.
-   No: nega all'utente la registrazione degli URL.

</dd> <dt>

<span id="_delegate__yes_no__"></span><span id="_DELEGATE__YES_NO__"></span>**\[Delegato = {Yes \| No}\]**
</dt> <dd>

Specifica uno dei valori seguenti:

-   Sì: consente all'utente di delegare gli URL.
-   No: nega all'utente la delega degli URL. Si tratta del valore predefinito.

</dd> <dt>

<span id="_sddl__string"></span><span id="_SDDL__STRING"></span>
**[SDDL =] stringa**
</dt> <dd>

Specifica la stringa SDDL che descrive l'elenco DACL.

</dd> </dl>

## <a name="examples"></a>Esempio

* add urlacl url=https://+:80/MyUri user=DOMAIN\\ user

* add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user listen=yes

* add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user delegate=no

 
## <a name="see-also"></a>Vedere anche

* [Comandi netsh per HTTP](/windows-server/networking/technologies/netsh/netsh-http#add-urlacl)
 