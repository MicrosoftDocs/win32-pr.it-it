---
description: Recupera i risultati dell'analisi dall'oggetto InkDivider.
ms.assetid: 7fc2bb5a-172f-4f4e-84dd-e31925f86982
title: Funzione CallDivideResults
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResults
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 2e5f3060f261ba84b70272ed358a7c544f2b0e1582de310ed759b4ea40714359
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967760"
---
# <a name="calldivideresults-function"></a>Funzione CallDivideResults

Recupera i risultati dell'analisi [**dall'oggetto InkDivider.**](inkdivider-class.md)

Questa funzione non deve essere usata dal codice dell'applicazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI CallDivideResults(
  _In_  INT_PTR   hDivider,
  _Out_ int       aWordStrokeIds[],
  _Out_ int       aLineStrokeIds[],
  _Out_ int       aParagraphStrokeIds[],
  _Out_ int       aDrawingStrokeIds[],
  _Out_ SAFEARRAY **pastrWords,
  _Out_ SAFEARRAY **pastrLines,
  _Out_ SAFEARRAY **pastrParagraphs,
  _Out_ int       *aWordRotationCenterX,
  _Out_ int       *aWordRotationCenterY,
  _Out_ float     *aWordAngle,
  _Out_ int       *aLineRotationCenterX,
  _Out_ int       *aLineRotationCenterY,
  _Out_ float     *aLineAngle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDivider* \[ Pollici\]
</dt> <dd>

Handle per [**l'oggetto InkDivider.**](inkdivider-class.md)

</dd> <dt>

*aWordStrokeIds* \[ Cambio\]
</dt> <dd>

Matrice di identificatori associati alla parola passata alla [**classe InkDivider.**](inkdivider-class.md)

</dd> <dt>

*aLineStrokeIds* \[ Cambio\]
</dt> <dd>

Matrice di [**proprietà ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) per gli oggetti [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) associati alla riga passata alla classe [**InkDivider.**](inkdivider-class.md)

</dd> <dt>

*aParagraphStrokeIds* \[ Cambio\]
</dt> <dd>

Matrice delle proprietà [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) per gli [**oggetti IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) associati al paragrafo dalla [**classe InkDivider.**](inkdivider-class.md)

</dd> <dt>

*aDrawingStrokeIds* \[ Cambio\]
</dt> <dd>

Matrice di [**proprietà ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) per gli oggetti [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) associati al disegno dalla classe [**InkDivider.**](inkdivider-class.md)

</dd> <dt>

*pastrWords* \[ Cambio\]
</dt> <dd>

Matrice di parole restituite dall'analisi dell'input penna.

</dd> <dt>

*pastrLines* \[ Cambio\]
</dt> <dd>

Matrice di righe restituite dall'analisi dell'input penna.

</dd> <dt>

*pastrParagraphs* \[ Cambio\]
</dt> <dd>

Matrice di paragrafi restituiti dall'analisi dell'input penna.

</dd> <dt>

*aWordRotationCenterX* \[ Cambio\]
</dt> <dd>

Matrice dei punti centrale delle parole lungo l'asse x dall'analisi dell'input penna.

</dd> <dt>

*aWordRotationCenterY* \[ Cambio\]
</dt> <dd>

Matrice dei punti centrale delle parole lungo l'asse y dall'analisi dell'input penna.

</dd> <dt>

*aWordAngle* \[ Cambio\]
</dt> <dd>

Matrice contenente gli angoli in base ai quali ruotare le parole per ottenere risultati di analisi ottimali.

</dd> <dt>

*aLineRotationCenterX* \[ Cambio\]
</dt> <dd>

Matrice contenente i punti centrale delle linee lungo l'asse x.

</dd> <dt>

*aLineRotationCenterY* \[ Cambio\]
</dt> <dd>

Matrice contenente i punti centrale delle linee lungo l'asse y.

</dd> <dt>

*aLineAngle* \[ Cambio\]
</dt> <dd>

Matrice contenente gli angoli in base ai quali ruotare le linee per ottenere risultati di analisi ottimali.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Funzione completata.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro hDivider* non è valido.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Impossibile allocare memoria sufficiente per archiviare i risultati.<br/> |



 

## <a name="remarks"></a>Commenti

Per evitare perdite di memoria, è necessario rilasciare le risorse per *pastrWords*, *pastrLines* e *pastrParagraphs*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                         |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Libreria<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




