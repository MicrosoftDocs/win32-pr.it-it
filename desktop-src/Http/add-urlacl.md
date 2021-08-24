---
title: add urlacl
description: Riserva l'URL specificato per gli account e gli utenti non amministratori.
ms.assetid: 5d89dec3-26e6-4db8-b4cc-e9b933ac60c5
keywords:
- add urlacl HTTP
topic_type:
- apiref
api_name:
- add urlacl
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: e3f4c715df70255ede8bd9ca5fc23131102983f8a3aeeb25735d5fc81d5ad9b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638781"
---
# <a name="add-urlacl"></a>add urlacl

Riserva l'URL specificato per gli account e gli utenti non amministratori. L'elenco di controllo di accesso discrezionale (DACL) può essere specificato usando un nome di account con i parametri listen e delegate oppure usando una stringa SDDL (Security Descriptor Definition Language).

``` syntax
add urlacl [url=]string
           [[user=]string
           {[[listen={yes|no}] [delegate={yes|no}]] | [sddl=]string}

 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>
**[url=] string**
</dt> <dd>

Specifica l'URL completo.

</dd> <dt>

<span id="_user__string"></span><span id="_USER__STRING"></span>
**[user=] string**
</dt> <dd>

Specifica il nome dell'utente o del gruppo di utenti.

</dd> <dt>

<span id="_listen__yes_no__"></span><span id="_LISTEN__YES_NO__"></span>**\[listen={yes \| no}\]**
</dt> <dd>

Specifica uno dei valori seguenti:

-   yes: consente all'utente di registrare gli URL. Si tratta del valore predefinito.
-   no: nega all'utente di registrare gli URL.

</dd> <dt>

<span id="_delegate__yes_no__"></span><span id="_DELEGATE__YES_NO__"></span>**\[delegate={yes \| no}\]**
</dt> <dd>

Specifica uno dei valori seguenti:

-   yes: consente all'utente di delegare gli URL.
-   no: nega all'utente di delegare gli URL. Si tratta del valore predefinito.

</dd> <dt>

<span id="_sddl__string"></span><span id="_SDDL__STRING"></span>
**[sddl=] string**
</dt> <dd>

Specifica la stringa SDDL che descrive l'elenco DACL.

</dd> </dl>

## <a name="examples"></a>Esempio

* add urlacl url=https://+:80/MyUri user=DOMAIN\\ user

* add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user listen=yes

* add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user delegate=no

 
## <a name="see-also"></a>Vedere anche

* [Comandi netsh per HTTP](/windows-server/networking/technologies/netsh/netsh-http#add-urlacl)
 