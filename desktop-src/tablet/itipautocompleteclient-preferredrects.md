---
description: Consente al client di suggerire dove posizionare l'elenco di completamento automatico per evitare la sovrapposizione del pannello di input.
ms.assetid: c82ffecb-f3e6-4c50-80bb-8393b39d3b2a
title: Metodo ITipAutocompleteClient::P referredRects (TipAutoComplete. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.PreferredRects
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 04e935c668e858ae3d22936e8a63f9116ebd6ab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315565"
---
# <a name="itipautocompleteclientpreferredrects-method"></a>ITipAutocompleteClient::P metodo referredRects

Consente al client di suggerire dove posizionare l'elenco di completamento automatico per evitare la sovrapposizione del pannello di input.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PreferredRects(
  [in]      RECT *prcACList,
  [in]      RECT *prcField,
  [out]     RECT *prcModified,
  [in, out] BOOL *pfShownAboveTip
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*prcACList* \[ in\]
</dt> <dd>

Rettangolo, in coordinate dello schermo, che indica la posizione preferita del provider e le dimensioni dell'interfaccia utente dell'elenco di completamento automatico.

</dd> <dt>

*prcField* \[ in\]
</dt> <dd>

Rettangolo, in coordinate dello schermo, che indica la posizione e le dimensioni del campo attivo.

</dd> <dt>

*prcModified* \[ out\]
</dt> <dd>

Rettangolo basato sullo stato corrente della Mancia e il percorso e la dimensione dell'elenco di completamento automatico preferiti specificati da *prcACList*.

</dd> <dt>

*pfShownAboveTip* \[ in uscita\]
</dt> <dd>

**True** se il rettangolo modificato deve essere visualizzato sopra l'area di destinazione del pannello di input di testo; in caso contrario, **false**. Questo valore deve essere inizializzato in modo da consentire l'orientamento preferito del provider prima che venga chiamato il metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                  | Descrizione                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Esito positivo.<br/>                                                                                                                                                                                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Chiamare il [**Metodo ITipAutocompleteClient:: RequestShowUI**](itipautocompleteclient-requestshowui.md) per impostare la finestra elenco popup automatico completato prima di chiamare il [**metodo ITipAutocompleteClient::P referredrects**](itipautocompleteclient-preferredrects.md).<br/> |
| <dl> <dt>**E \_ non riescono**</dt> </dl>       | Si è verificato un errore non specificato.<br/>                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Commenti

Si tratta del metodo chiamato dal provider di completamento automatico quando sta per visualizzare l'interfaccia utente di completamento automatico. Il client modifica il rettangolo preferito del provider specificato da *prcACList* tramite l'argomento *prcModified* .

Chiamare il [**Metodo ITipAutocompleteClient:: RequestShowUI**](itipautocompleteclient-requestshowui.md) per impostare l'handle della finestra elenco di completamento automatico popup prima di chiamare **PreferredRects**. In caso contrario, viene generato un errore **E \_ INVALIDARG** quando si chiama **PreferredRects**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                                   |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                       |
| Intestazione<br/>                   | <dl> <dt>TipAutoComplete. h (richiede anche PenInputPanel \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITipAutocompleteClient**](itipautocompleteclient.md)
</dt> <dt>

[**Metodo ITipAutocompleteClient:: RequestShowUI**](itipautocompleteclient-requestshowui.md)
</dt> <dt>

[Riferimento al pannello input di testo](text-input-panel-reference.md)
</dt> </dl>

 

 




