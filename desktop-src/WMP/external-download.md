---
title: Metodo External.download
description: Nota Questo argomento descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di uno store online non è supportato. Il metodo di download avvia il download di un set di elementi multimediali.
ms.assetid: 10bae41c-0658-4712-8a7e-375a1ec6dc25
keywords:
- Metodo di download Windows Media Player
- metodo download Windows Media Player , classe external
- Classe esterna Windows Media Player , metodo download
topic_type:
- apiref
api_name:
- External.download
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 766f96a6db5f2114724e7545eaac7a269bf52e2e657872a8078b490621c794df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649221"
---
# <a name="externaldownload-method"></a>Metodo External.download

> [!Note]  
> In questo argomento vengono descritte le funzionalità progettate per l'utilizzo da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di uno store online non è supportato.

 

Il **metodo di download** avvia il download di un set di elementi multimediali.

## <a name="syntax"></a>Sintassi


```JScript
External.download(
  Type,
  IDs
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tipo* \[ Pollici\]
</dt> <dd>

Costante [del percorso della](library-location-constants.md) libreria che specifica il tipo di elemento da scaricare. Ad esempio, CPTrackID specifica che devono essere scaricate una o più tracce.

</dd> <dt>

*ID* \[ Pollici\]
</dt> <dd>

**Stringa** contenente gli ID, delimitati da punti e virgola, degli elementi multimediali da scaricare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Download di contenuti multimediali**](downloading-media-content.md)
</dt> <dt>

[**Oggetto esterno per i negozi online di tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.buy**](external-buy.md)
</dt> <dt>

[**IWMPContentPartner::D ownload**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download)
</dt> </dl>

 

 





