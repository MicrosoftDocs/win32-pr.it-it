---
title: Funzione ImageList_SetColorTable
description: Imposta la tabella dei colori per un elenco di immagini.
ms.assetid: 1b62f468-cbc4-479b-b9f8-5553c2bd8c79
keywords:
- Controlli di Windows per la funzione ImageList_SetColorTable
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
ms.openlocfilehash: 14be5f17d83128933a35730a79726b462436e0c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103965020"
---
# <a name="imagelist_setcolortable-function"></a>ImageList \_ SetColorTable (funzione)

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

*himl* \[ in\]
</dt> <dd>

Tipo: **HIMAGELIST**

Handle per l'elenco di immagini.

</dd> <dt>

*inizio* \[ in\]
</dt> <dd>

Tipo: **int**

Indice della tabella dei colori in base zero che specifica la prima voce della tabella dei colori da impostare.

</dd> <dt>

*Len* \[ in\]
</dt> <dd>

Tipo: **int**

Numero di voci della tabella dei colori da impostare.

</dd> <dt>

*prgb* \[ in\]
</dt> <dd>

Tipo: **[**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) \** _

Puntatore a una matrice di strutture _len * [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) contenenti nuove informazioni sui colori per la tabella dei colori della DIB.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **int**

Se la funzione ha esito positivo, restituisce il numero di voci della tabella dei colori impostate dalla funzione. Se la funzione ha esito negativo, il valore restituito è minore o uguale a zero.

## <a name="remarks"></a>Commenti

Solo gli elenchi di immagini creati con il flag [**ILC \_ COLOR4**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) o [**ILC \_ COLOR8**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) hanno tabelle dei colori. La tabella dei colori di un elenco di immagini di questo tipo viene in genere impostata automaticamente copiando la tabella dei colori della prima immagine aggiunta all'elenco (ad esempio, tramite la funzione di [**\_ aggiunta ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) ) se l'immagine è una DIB. Se la prima immagine aggiunta all'elenco di immagini non è una DIB, viene usata la tabella dei colori della tavolozza mezzitoni per gli elenchi di immagini **\_ COLOR8 di ILC** e viene usata la tabella dei colori VGA per **ILC \_ COLOR4**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                                  |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versione 3,51 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tabella colori](https://msdn.microsoft.com/library/ms531197(v=VS.85).aspx)
</dt> </dl>

 

