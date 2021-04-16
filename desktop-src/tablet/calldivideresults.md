---
description: Recupera i risultati dell'analisi dall'oggetto InkDivider.
ms.assetid: 7fc2bb5a-172f-4f4e-84dd-e31925f86982
title: CallDivideResults (funzione)
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
ms.openlocfilehash: 11878e6a0ac953b9b7eb27ce21bb67001f9d88d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127819"
---
# <a name="calldivideresults-function"></a>CallDivideResults (funzione)

Recupera i risultati dell'analisi dall'oggetto [**InkDivider**](inkdivider-class.md) .

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

*hDivider* \[ in\]
</dt> <dd>

Handle per l'oggetto [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*aWordStrokeIds* \[ out\]
</dt> <dd>

Matrice di identificatori associati alla parola passata alla classe [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*aLineStrokeIds* \[ out\]
</dt> <dd>

Matrice di proprietà [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) per gli oggetti [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) associati alla riga passata alla classe [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*aParagraphStrokeIds* \[ out\]
</dt> <dd>

Matrice delle proprietà [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) per gli oggetti [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) associati al paragrafo dalla classe [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*aDrawingStrokeIds* \[ out\]
</dt> <dd>

Matrice di proprietà [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) per gli oggetti [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) associati al disegno dalla classe [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*pastrWords* \[ out\]
</dt> <dd>

Matrice di parole restituita dall'analisi dell'input penna.

</dd> <dt>

*pastrLines* \[ out\]
</dt> <dd>

Matrice di righe restituite dall'analisi dell'input penna.

</dd> <dt>

*pastrParagraphs* \[ out\]
</dt> <dd>

Matrice di paragrafi restituiti dall'analisi dell'input penna.

</dd> <dt>

*aWordRotationCenterX* \[ out\]
</dt> <dd>

Matrice dei punti centrali delle parole lungo l'asse x dall'analisi dell'input penna.

</dd> <dt>

*aWordRotationCenterY* \[ out\]
</dt> <dd>

Matrice dei punti centrali delle parole lungo l'asse y dell'analisi dell'input penna.

</dd> <dt>

*aWordAngle* \[ out\]
</dt> <dd>

Matrice contenente gli angoli in base ai quali ruotare le parole per ottenere risultati di analisi ottimali.

</dd> <dt>

*aLineRotationCenterX* \[ out\]
</dt> <dd>

Matrice contenente i punti centrali delle linee lungo l'asse x.

</dd> <dt>

*aLineRotationCenterY* \[ out\]
</dt> <dd>

Matrice contenente i punti centrali delle linee lungo l'asse y.

</dd> <dt>

*aLineAngle* \[ out\]
</dt> <dd>

Matrice contenente gli angoli in base ai quali ruotare le linee per ottenere risultati di analisi ottimali.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Funzione completata.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il parametro *hDivider* non è valido.<br/>                   |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Non è stato possibile allocare memoria sufficiente per archiviare i risultati.<br/> |



 

## <a name="remarks"></a>Commenti

Per evitare perdite di memoria, è necessario rilasciare le risorse per *pastrWords*, *pastrLines* e *pastrParagraphs*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                         |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Libreria<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




