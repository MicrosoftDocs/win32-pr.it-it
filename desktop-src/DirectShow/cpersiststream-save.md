---
description: Salva i dati del filtro nel flusso specificato.
ms.assetid: f45c8c6e-f0bb-4358-805a-da2669706d34
title: Metodo CPersistStream. Save (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.Save
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c16e4820f846d2d60382fabd6aafe3ad82880193
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328924"
---
# <a name="cpersiststreamsave-method"></a>Metodo CPersistStream. Save

Salva i dati del filtro nel flusso specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Save(
   LPSTREAM pStm,
   BOOL     fClearDirty
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStm* 
</dt> <dd>

Puntatore al flusso in cui salvare i dati.

</dd> <dt>

*fClearDirty* 
</dt> <dd>

Flag che indica se reimpostare il flag Dirty del flusso corrente; **True** indica di reimpostarlo. Quando il metodo viene chiamato come parte di un'operazione di salvataggio, il valore è in genere **true**; quando viene chiamato come parte di un'operazione Save As, il valore è in genere **false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il metodo **IPersistStream:: Save** . Chiama **WriteInt** con la versione del software, chiama [**CPersistStream:: WriteToStream**](cpersiststream-writetostream.md) con il flusso in *pstm* e Reimposta **mPS \_ fDirty**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PStream. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




