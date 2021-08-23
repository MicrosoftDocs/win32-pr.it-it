---
title: External.accountType
description: Nota In questo argomento vengono descritte le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato. La proprietà accountType recupera il tipo di account dell'utente corrente.
ms.assetid: 4fb6de90-a32d-4483-bbae-b23cbff93bd5
keywords:
- External.accountType Windows Media Player
topic_type:
- apiref
api_name:
- External.accountType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bd19413d891f5a8008b162f6795af29a9d15e75a80d35bb82ff13f8e013da9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650041"
---
# <a name="externalaccounttype"></a>External.accountType

> [!Note]  
> Questo argomento descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato.

 

La **proprietà accountType** recupera il tipo di account dell'utente corrente.

``` syntax
window.external.accountType
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una stringa di sola **lettura che** rappresenta il tipo di account. Le stringhe che rappresentano vari tipi di account vengono definite dal negozio online.

## <a name="remarks"></a>Commenti

Questa proprietà recupera il tipo di account chiamando il metodo [IWMPContentPartner::GetContentPartnerInfo,](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo) implementato dal plug-in dello store online. Se l'utente corrente è connesso al negozio online o il plug-in ha memorizzato nella cache le credenziali dell'utente, il **metodo getContentPartnerInfo** può determinare il tipo di account dell'utente e restituirlo Windows Media Player. Il tipo di account è una stringa Windows Media Player non interpreta. Al contrario, Windows Media Player la stringa dal plug-in del negozio online allo script nella pagina di individuazione del negozio online.

Se l'utente corrente non è connesso al negozio online e il plug-in del negozio online non dispone di credenziali memorizzate nella cache per l'utente, questa proprietà recupera qualsiasi stringa restituita dal metodo **getContentPartnerInfo** in tale situazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi online di tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.userLoggedIn**](external-userloggedin.md)
</dt> </dl>

 

 





