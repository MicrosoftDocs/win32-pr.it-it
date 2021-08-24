---
title: MM_ACM_FORMATCHOOSE messaggio (Msacm.h)
description: Il messaggio MM ACM FORMATCHOOSE invia una notifica a una funzione hook della finestra di dialogo \_ acmFormatChoose prima di aggiungere un elemento a una delle tre caselle \_ di riepilogo a discesa.
ms.assetid: f77e41c6-14e9-45c0-971e-4d6325145f1c
keywords:
- MM_ACM_FORMATCHOOSE messaggio Windows Multimedia
topic_type:
- apiref
api_name:
- MM_ACM_FORMATCHOOSE
api_location:
- Msacm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cceaa67bc0ce4ee922b48d1cff20eb2bf6414f93506dcc70ccd6e0e912211544
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119782961"
---
# <a name="mm_acm_formatchoose-message"></a>MM \_ ACM \_ FORMATCHOOSE message

Il **messaggio MM \_ ACM \_ FORMATCHOOSE** invia una notifica a una funzione hook della finestra di dialogo [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) prima di aggiungere un elemento a una delle tre caselle di riepilogo a discesa. Questo messaggio consente a un'applicazione di personalizzare ulteriormente le selezioni disponibili tramite l'interfaccia utente.


```C++
MM_ACM_FORMATCHOOSE 
wParam = (WPARAM) wDropDown 
lParam = (LONG) lCustom 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*
</dt> <dd>

Casella di riepilogo a discesa da inizializzare e operazione di verifica o aggiunta.



| Requisito | Valore |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FORMATCHOOSE \_ CUSTOM \_ VERIFY    | Il *parametro lParam* è un puntatore a [**una struttura WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) da aggiungere alla casella di riepilogo a discesa Nome personalizzata.                                                                                                   |
| FORMATCHOOSE \_ FORMAT \_ ADD       | Il *parametro lParam* è un puntatore a un buffer che accetterà una struttura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) da aggiungere alla casella di riepilogo a discesa Formato. L'applicazione deve copiare la struttura del formato da aggiungere in questo buffer. |
| FORMATCHOOSE \_ FORMAT \_ VERIFY    | Il *parametro lParam* è un puntatore a [**una struttura WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) da aggiungere alla casella di riepilogo a discesa Formato.                                                                                                        |
| FORMATCHOOSE \_ FORMATTAG \_ ADD    | Il *parametro lParam* è un puntatore a una variabile che accetterà un tag di formato audio waveform da aggiungere alla casella di riepilogo a discesa Tag di formato.                                                                                             |
| FORMATCHOOSE \_ FORMATTAG \_ VERIFY | Il *parametro lParam* è un tag di formato audio waveform da elencare nell'elenco a discesa Tag di formato.                                                                                                                                     |



 

</dd> <dt>

<span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*
</dt> <dd>

Valore definito dalla casella di riepilogo specificata nel **parametro wParam.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** un'applicazione gestisce questo messaggio o FALSE in caso **contrario.**

## <a name="remarks"></a>Commenti

Se l'applicazione elabora l'operazione ADD FILTERCHOOSE FORMAT, le dimensioni del buffer di memoria fornito in lParam verranno determinate dalla \_ \_ funzione [**acmMetrics.**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) 

Se l'applicazione sta elaborando un'operazione di verifica, può impedire alla finestra di dialogo di elencare questa selezione chiamando la **funzione SetWindowLong** con *nIndex* impostato su DWL \_ MSGRESULT e *lNewLong* impostato su **FALSE** (cast a un tipo di dati **LONG).** Per consentire alla finestra di dialogo di elencare questa selezione, chiamare questa funzione con *lNewLong* impostato su **TRUE.**

Se l'applicazione sta elaborando un'operazione di aggiunta, può indicare che non sono necessarie altre aggiunte chiamando la **funzione SetWindowLong** con *nIndex* impostato su DWL \_ MSGRESULT e *lNewLong* impostato su **FALSE** (cast a un tipo di dati **LONG).** Per indicare che sono necessarie altre aggiunte, chiamare questa funzione con *lNewLong* impostato su **TRUE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Msacm.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione compressione audio](audio-compression-manager.md)
</dt> <dt>

[Messaggi di compressione audio](audio-compression-messages.md)
</dt> </dl>

 

