---
title: Aggiorna comando
description: Il comando Update ridisegna il frame corrente nel contesto di dispositivo specificato (DC). I dispositivi digitali video riconoscono questo comando.
ms.assetid: 51a83262-91d5-4852-ad17-bd62c14417b1
keywords:
- Aggiorna il comando Windows Multimedia
topic_type:
- apiref
api_name:
- update
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cb0fc96d404efd8e2f657985ffa5a8861d3b4f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518963"
---
# <a name="update-command"></a>Aggiorna comando

Il comando Update ridisegna il frame corrente nel contesto di dispositivo specificato (DC). I dispositivi digitali video riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("update %s %s %s"), 
  lpszDeviceID, 
  lpszHDC, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszHDC"></span><span id="lpszhdc"></span><span id="LPSZHDC"></span>*lpszHDC*
</dt> <dd>

Handle di un controller di dominio. Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando di **aggiornamento** e i flag utilizzati da ogni tipo.



| Valore        | Significato                       | Significato         |
|--------------|-------------------------------|-----------------|
| digitalvideo | HDC *HDC HDC hdc*  in *Rect* | Paint HDC *HDC* |



 

Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszHDC** e i relativi significati.



| Valore               | Significato                                                                                                |
|---------------------|--------------------------------------------------------------------------------------------------------|
| HDC *HDC*           | Specifica l'handle del controller di dominio da disegnare.                                                               |
| HDC *HDC* in *Rect* | Specifica il rettangolo di ridimensionamento rispetto al rettangolo client.                                     |
| Paint HDC *HDC*     | Disegna il controller di dominio quando l'applicazione riceve un messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) destinato a un controller di dominio. |



 

Per specificare l'handle del controller di dominio, usare la stringa "HDC" seguita da una rappresentazione ASCII dell'handle. Il rettangolo viene specificato come **X1 Y1 Y1 2**. Le coordinate **X1 Y1** specificano l'angolo superiore sinistro del rettangolo e le coordinate **X2 Y2** specificano la larghezza e l'altezza.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify" o entrambi. Per i dispositivi digitali video è possibile specificare anche "test". Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="examples"></a>Esempio

Il comando seguente aggiorna l'intera finestra di visualizzazione usata dal dispositivo "Movie". Il numero 203 è un handle per un controller di dominio ottenuto dalla funzione [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) .

``` syntax
update movie hdc 203
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> </dl>

 

