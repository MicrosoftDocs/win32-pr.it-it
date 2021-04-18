---
title: Metodo External. download
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. Il metodo di download avvia il download di un set di elementi multimediali.
ms.assetid: 10bae41c-0658-4712-8a7e-375a1ec6dc25
keywords:
- Metodo di download Media Player Windows
- Metodo di download Media Player Windows, classe esterna
- Classe esterna Media Player Windows, metodo di download
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
ms.openlocfilehash: 35ef0c6e6c32e8959e402080796f29a3860fe728
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324566"
---
# <a name="externaldownload-method"></a>Metodo External. download

> [!Note]  
> Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

Il metodo di **download** avvia il download di un set di elementi multimediali.

## <a name="syntax"></a>Sintassi


```JScript
External.download(
  Type,
  IDs
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tipo* \[ di in\]
</dt> <dd>

[Costante del percorso della libreria](library-location-constants.md) che specifica il tipo di elemento da scaricare. Ad esempio, CPTrackID specifica che devono essere scaricate una o più tracce.

</dd> <dt>

*ID* \[ di in\]
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

[**Download del contenuto multimediale**](downloading-media-content.md)
</dt> <dt>

[**Oggetto esterno per i negozi di tipo 1 online**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. Buy**](external-buy.md)
</dt> <dt>

[**IWMPContentPartner::D ownload**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download)
</dt> </dl>

 

 





