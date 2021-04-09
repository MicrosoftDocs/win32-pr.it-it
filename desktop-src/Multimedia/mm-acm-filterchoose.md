---
title: Messaggio MM_ACM_FILTERCHOOSE (Msacm. h)
description: Il \_ messaggio mm ACM \_ FILTERCHOOSE notifica a una funzione di hook della finestra di dialogo acmFilterChoose prima di aggiungere un elemento a una delle tre caselle di riepilogo a discesa.
ms.assetid: f3c68240-a9aa-4771-96b9-1cb3bb5ea906
keywords:
- MM_ACM_FILTERCHOOSE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_ACM_FILTERCHOOSE
api_location:
- Msacm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1df28ad7f950b8ce995fd308622db8c429393cb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119143"
---
# <a name="mm_acm_filterchoose-message"></a>MM \_ \_ FILTERCHOOSE del messaggio ACM

Il messaggio **mm \_ ACM \_ FILTERCHOOSE** notifica a una funzione di hook della finestra di dialogo [**acmFilterChoose**](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose) prima di aggiungere un elemento a una delle tre caselle di riepilogo a discesa. Questo messaggio consente a un'applicazione di personalizzare ulteriormente le selezioni disponibili tramite l'interfaccia utente.


```C++
        MM_ACM_FILTERCHOOSE
        wParam = (WPARAM) wDropDown
        lParam = (LONG) lCustom
      
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*
</dt> <dd>

Casella di riepilogo a discesa inizializzata e operazione di verifica o di aggiunta.



| Requisito | Valore |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_verifica personalizzata di FILTERCHOOSE \_    | Il parametro *lParam* è un puntatore a una struttura [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) da aggiungere alla casella di riepilogo a discesa nome personalizzato.                                                                                                   |
| \_aggiunta filtro \_ FILTERCHOOSE       | Il parametro *lParam* è un puntatore a un buffer che accetterà una struttura [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) da aggiungere all'elenco a discesa del filtro. L'applicazione deve copiare la struttura del filtro da aggiungere in questo buffer. |
| \_Verifica del filtro FILTERCHOOSE \_    | Il parametro *lParam* è un puntatore a una struttura [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) da aggiungere alla casella di riepilogo a discesa filtro.                                                                                                        |
| \_aggiunta FILTERCHOOSE FILTERTAG \_    | Il parametro *lParam* è un puntatore a un **valore DWORD** che accetterà un tag di filtro della forma d'onda-audio da aggiungere alla casella di riepilogo a discesa Tag filtro.                                                                                        |
| \_Verifica FILTERTAG \_ FILTERCHOOSE | Il parametro *lParam* è un tag del filtro per la forma d'onda, che deve essere elencato nella casella di riepilogo a discesa Tag filtro.                                                                                                                                 |



 

</dd> <dt>

<span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*
</dt> <dd>

Valore definito dalla casella di riepilogo specificata nel parametro **wParam** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se un'applicazione gestisce questo messaggio o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Se l'applicazione elabora l' \_ \_ operazione di aggiunta del filtro FILTERCHOOSE, le dimensioni del buffer di memoria fornito in *lParam* verranno determinate dalla funzione [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) .

Se l'applicazione elabora un'operazione di verifica, l'applicazione deve precedere il valore restituito con **SetWindowLong** (HWND, DWL \_ MSGRESULT, (Long) **false**) per impedire che la finestra di dialogo elenchi questa selezione o con **SetWindowLong** (HWND, DWL \_ MSGRESULT, (Long)**true**) per consentire alla finestra di dialogo di elencare questa selezione. Se si elabora un'operazione di aggiunta, l'applicazione deve precedere la restituzione con **SetWindowLong** (HWND, DWL \_ MSGRESULT, (Long)**false**) per indicare che non sono necessarie altre aggiunte o con **SetWindowLong** (HWND, DWL \_ MSGRESULT, (Long)**true**) se sono necessarie altre aggiunte.

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

 

 





