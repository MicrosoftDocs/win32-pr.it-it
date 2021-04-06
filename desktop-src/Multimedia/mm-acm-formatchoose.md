---
title: Messaggio MM_ACM_FORMATCHOOSE (Msacm. h)
description: Il \_ messaggio mm ACM \_ FORMATCHOOSE notifica a una funzione hook della finestra di dialogo acmFormatChoose prima di aggiungere un elemento a una delle tre caselle di riepilogo a discesa.
ms.assetid: f77e41c6-14e9-45c0-971e-4d6325145f1c
keywords:
- MM_ACM_FORMATCHOOSE messaggi multimediali di Windows
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
ms.openlocfilehash: 35808e06521cbd83d07f8d6c799779a16f50236b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743922"
---
# <a name="mm_acm_formatchoose-message"></a>MM \_ \_ FORMATCHOOSE del messaggio ACM

Il messaggio **mm \_ ACM \_ FORMATCHOOSE** notifica a una funzione hook della finestra di dialogo [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) prima di aggiungere un elemento a una delle tre caselle di riepilogo a discesa. Questo messaggio consente a un'applicazione di personalizzare ulteriormente le selezioni disponibili tramite l'interfaccia utente.


```C++
MM_ACM_FORMATCHOOSE 
wParam = (WPARAM) wDropDown 
lParam = (LONG) lCustom 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*
</dt> <dd>

Casella di riepilogo a discesa inizializzata e operazione di verifica o di aggiunta.



| Requisito | Valore |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_verifica personalizzata di FORMATCHOOSE \_    | Il parametro *lParam* è un puntatore a una struttura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) da aggiungere alla casella di riepilogo a discesa nome personalizzato.                                                                                                   |
| \_aggiunta formato \_ FORMATCHOOSE       | Il parametro *lParam* è un puntatore a un buffer che accetterà una struttura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) da aggiungere alla casella di riepilogo a discesa formato. L'applicazione deve copiare la struttura del formato da aggiungere in questo buffer. |
| \_verifica formato \_ FORMATCHOOSE    | Il parametro *lParam* è un puntatore a una struttura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) da aggiungere alla casella di riepilogo a discesa formato.                                                                                                        |
| \_aggiunta FORMATCHOOSE FORMATTAG \_    | Il parametro *lParam* è un puntatore a una variabile che accetterà un tag di formato Waveform-Audio da aggiungere alla casella di riepilogo a discesa Tag di formato.                                                                                             |
| \_Verifica FORMATTAG \_ FORMATCHOOSE | Il parametro *lParam* è un tag di formato della forma d'onda-audio da elencare nell'elenco a discesa Tag di formato.                                                                                                                                     |



 

</dd> <dt>

<span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*
</dt> <dd>

Valore definito dalla casella di riepilogo specificata nel parametro **wParam** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se un'applicazione gestisce questo messaggio o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Se l'applicazione elabora l' \_ \_ operazione di aggiunta del formato FILTERCHOOSE, le dimensioni del buffer di memoria fornito in *lParam* verranno determinate dalla funzione [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) .

Se l'applicazione sta elaborando un'operazione di verifica, può impedire alla finestra di dialogo di elencare questa selezione chiamando la funzione **SetWindowLong** con *NINDEX* impostato su DWL \_ MSGRESULT e *lNewLong* impostato su **false** (eseguito il cast a un tipo di dati **Long** ). Per consentire alla finestra di dialogo di elencare questa selezione, chiamare questa funzione con *lNewLong* impostato su **true**.

Se l'applicazione sta elaborando un'operazione di aggiunta, può indicare che non sono necessarie altre aggiunte chiamando la funzione **SetWindowLong** con *NINDEX* impostato su DWL \_ MSGRESULT e *lNewLong* impostato su **false** (eseguito il cast a un tipo di dati **Long** ). Per indicare che sono necessarie altre aggiunte, chiamare questa funzione con *lNewLong* impostato su **true**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Msacm. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione compressione audio](audio-compression-manager.md)
</dt> <dt>

[Messaggi di compressione audio](audio-compression-messages.md)
</dt> </dl>

 

