---
title: External. accountType
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. La proprietà accountType Recupera il tipo di account dell'utente corrente.
ms.assetid: 4fb6de90-a32d-4483-bbae-b23cbff93bd5
keywords:
- Media Player di Windows External. accountType
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
ms.openlocfilehash: 16fce659f38af19157536a4bf763362c35fc9dfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329933"
---
# <a name="externalaccounttype"></a>External. accountType

> [!Note]  
> Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

La proprietà **AccountType** Recupera il tipo di account dell'utente corrente.

``` syntax
window.external.accountType
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una **stringa** di sola lettura che rappresenta il tipo di conto. Le stringhe che rappresentano i diversi tipi di conto sono definite dall'archivio online.

## <a name="remarks"></a>Commenti

Questa proprietà recupera il tipo di conto chiamando il metodo [IWMPContentPartner:: GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo) , che viene implementato dal plug-in del negozio online. Se l'utente corrente è connesso allo Store online oppure il plug-in ha memorizzato nella cache le credenziali dell'utente, il metodo **getContentPartnerInfo** può determinare il tipo di account dell'utente e restituirlo a Windows Media Player. Il tipo di account è una stringa che Windows Media Player non interpreta. Windows Media Player invece passa la stringa dal plug-in Online Store allo script nella pagina di individuazione del negozio online.

Se l'utente corrente non è connesso allo Store online e il plug-in del negozio online non dispone di credenziali memorizzate nella cache per l'utente, questa proprietà recupera qualsiasi stringa restituita dal metodo **getContentPartnerInfo** in tale situazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi di tipo 1 online**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. userLoggedIn**](external-userloggedin.md)
</dt> </dl>

 

 





