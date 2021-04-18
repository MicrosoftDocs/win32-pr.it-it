---
title: External. viewParameters
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | External. viewParameters
ms.assetid: 0afabe35-2857-413a-a662-1a76d3fb75fe
keywords:
- Media Player di Windows External. viewParameters
topic_type:
- apiref
api_name:
- External.viewParameters
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0adec580a68bd3f6b92beef1de814729848179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328396"
---
# <a name="externalviewparameters"></a>External. viewParameters

> [!Note]  
> Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

La proprietà **viewParameters** recupera i parametri associati alla visualizzazione corrente in Windows Media Player.

## <a name="syntax"></a>Sintassi

**finestra. External. viewParameters**

## <a name="possible-values"></a>Valori possibili

Questa proprietà restituisce una **stringa** di sola lettura.

## <a name="remarks"></a>Commenti

Questa proprietà recupera i parametri impostati in precedenza dal negozio online. Ad esempio, l'archivio online può specificare i parametri di visualizzazione nel parametro *ViewParams* del metodo [changeView](external-changeview.md) o il parametro *params* del metodo [changeViewOnlineList](external-changeviewonlinelist.md) .

I parametri di visualizzazione non vengono interpretati da Windows Media Player. Vengono creati dal negozio online e hanno un significato solo per lo Store online.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi di tipo 1 online**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





