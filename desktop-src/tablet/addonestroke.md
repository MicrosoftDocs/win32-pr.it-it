---
description: Aggiunge un nuovo oggetto IInkStrokeDisp all'oggetto InkDivider passato.
ms.assetid: d5b82244-68d5-4137-aaf4-d3232f7c0779
title: AddOneStroke (funzione)
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
ms.openlocfilehash: 0af3913f2579363afbb0c3985ad0f40f58051eac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483997"
---
# <a name="addonestroke-function"></a>AddOneStroke (funzione)

Aggiunge un nuovo oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) all'oggetto [**InkDivider**](inkdivider-class.md) passato.

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

*hDivider* \[ in\]
</dt> <dd>

Handle per l'oggetto [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*strokeId* \[ in\]
</dt> <dd>

[**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) dell'oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) da aggiungere all'oggetto [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*cPoints* \[ in\]
</dt> <dd>

Il numero di pacchetti che costituiscono il nuovo oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .

</dd> <dt>

*aPoints* \[ in\]
</dt> <dd>

Matrice di pacchetti che costituiscono l'oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) in *strokeId*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione può restituire uno di questi valori.



| Codice restituito                                                                                  | Descrizione                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Funzione completata.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il parametro *hDivider* non è valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                         |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Libreria<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




