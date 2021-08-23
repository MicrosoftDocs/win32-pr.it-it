---
title: ImageList_SetColorTable funzione
description: Imposta la tabella dei colori per un elenco di immagini.
ms.assetid: 1b62f468-cbc4-479b-b9f8-5553c2bd8c79
keywords:
- ImageList_SetColorTable funzione Windows controlli
topic_type:
- apiref
api_name:
- ImageList_SetColorTable
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de1acd8f14d9993bc75ea69b910b365e29156a6386933ccb95251a916c37244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412239"
---
# <a name="imagelist_setcolortable-function"></a>Funzione ImageList \_ SetColorTable

Imposta la tabella dei colori per un elenco di immagini.

## <a name="syntax"></a>Sintassi


```C++
int ImageList_SetColorTable(
  _In_ HIMAGELIST himl,
  _In_ int        start,
  _In_ int        len,
  _In_ RGBQUAD    *prgb
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*himl* \[ Pollici\]
</dt> <dd>

Tipo: **HIMAGELIST**

Handle per l'elenco di immagini.

</dd> <dt>

*start* \[ Pollici\]
</dt> <dd>

Tipo: **int**

Indice della tabella dei colori in base zero che specifica la prima voce della tabella dei colori da impostare.

</dd> <dt>

*len* \[ Pollici\]
</dt> <dd>

Tipo: **int**

Numero di voci della tabella dei colori da impostare.

</dd> <dt>

*prgb* \[ Pollici\]
</dt> <dd>

Tipo: **[ **RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad)\***

Puntatore a una matrice di strutture [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) *len* contenenti nuove informazioni sul colore per la tabella dei colori della DIB.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **int**

Se la funzione ha esito positivo, restituisce il numero di voci della tabella dei colori impostate dalla funzione. Se la funzione ha esito negativo, il valore restituito è minore o uguale a zero.

## <a name="remarks"></a>Commenti

Solo gli elenchi di immagini creati con il flag [**ILC \_ COLOR4**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) o [**ILC \_ COLOR8**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) hanno tabelle colori. La tabella dei colori di tale elenco di immagini viene in genere impostata automaticamente copiando la tabella dei colori della prima immagine aggiunta all'elenco (ad esempio, tramite la funzione [**ImageList \_ Add)**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) se tale immagine è di tipo DIB. Se la prima immagine aggiunta all'elenco immagini non è di tipo DIB, la tabella dei colori della tavolozza dei mezzitoni viene usata per gli elenchi di immagini **ILC \_ COLOR8** e la tabella dei colori VGA viene usata per **ILC \_ COLOR4.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                                  |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versione 3.51 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tabella dei colori](https://msdn.microsoft.com/library/ms531197(v=VS.85).aspx)
</dt> </dl>

 

