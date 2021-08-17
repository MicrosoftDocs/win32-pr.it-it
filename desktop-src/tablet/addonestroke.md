---
description: Aggiunge un nuovo oggetto IInkStrokeDisp all'oggetto InkDivider passato.
ms.assetid: d5b82244-68d5-4137-aaf4-d3232f7c0779
title: Funzione AddOneStroke
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddOneStroke
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 431043b261b3e6fa67e8c6c9e45df27bb6c252dfd92b18e0e4127d4795533c0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857130"
---
# <a name="addonestroke-function"></a>Funzione AddOneStroke

Aggiunge un [**nuovo oggetto IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) [**all'oggetto InkDivider**](inkdivider-class.md) passato.

Questa funzione non deve essere usata dal codice dell'applicazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI AddOneStroke(
  _In_ INT_PTR hDivider,
  _In_ int     strokeId,
  _In_ int     cPoints,
  _In_ POINT   *aPoints
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDivider* \[ Pollici\]
</dt> <dd>

Handle per [**l'oggetto InkDivider.**](inkdivider-class.md)

</dd> <dt>

*strokeId* \[ Pollici\]
</dt> <dd>

ID [**dell'oggetto**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) da aggiungere all'oggetto [**InkDivider.**](inkdivider-class.md)

</dd> <dt>

*cPoints* \[ Pollici\]
</dt> <dd>

Numero di pacchetti che costituiscono il nuovo [**oggetto IInkStrokeDisp.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)

</dd> <dt>

*aPoints* \[ Pollici\]
</dt> <dd>

Matrice di pacchetti che costituiscono l'oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) in *strokeId*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione può restituire uno di questi valori.



| Codice restituito                                                                                  | Descrizione                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Funzione completata.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il *parametro hDivider* non è valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                         |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Libreria<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




