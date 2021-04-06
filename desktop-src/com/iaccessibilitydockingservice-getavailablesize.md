---
title: Metodo IAccessibilityDockingService GetAvailableSize
description: Ottiene le dimensioni disponibili per l'ancoraggio di una finestra di accessibilità su un monitor.
ms.assetid: 1C838B01-EF26-4FCC-878F-A36DEFBA3142
keywords:
- Metodo GetAvailableSize COM
- Metodo GetAvailableSize COM, interfaccia IAccessibilityDockingService
- Interfaccia IAccessibilityDockingService COM, metodo GetAvailableSize
topic_type:
- apiref
api_name:
- IAccessibilityDockingService.GetAvailableSize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1b9f113792b14f5fb86e0349d083ea48ffdb3fd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045682"
---
# <a name="iaccessibilitydockingservicegetavailablesize-method"></a>Metodo IAccessibilityDockingService:: GetAvailableSize

Ottiene le dimensioni disponibili per l'ancoraggio di una finestra di accessibilità su un monitor.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAvailableSize(
  [in]  HMONITOR hMonitor,
  [out] UINT     *puMaxHeight,
  [out] UINT     *puFixedWidth
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hMonitor* \[ in\]
</dt> <dd>

Specifica il monitoraggio per cui verranno recuperate le dimensioni di ancoraggio disponibili.

</dd> <dt>

*puMaxHeight* \[ out\]
</dt> <dd>

Se l'operazione riesce, impostare sull'altezza massima disponibile per l'ancoraggio sul *hMonitor* specificato, in pixel.

In caso di errore, impostare su zero.

</dd> <dt>

*puFixedWidth* \[ out\]
</dt> <dd>

Se l'operazione riesce, impostare sulla larghezza fissa disponibile per l'ancoraggio sul *hMonitor* specificato, in pixel. Tutte le finestre ancorate a questo *hMonitor* verranno ridimensionate in base a questa larghezza.

In caso di errore, impostare su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito



| Codice restituito                                                                                                                          | Descrizione                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                                 | Esito positivo.<br/>                                                              |
| <dl> <dt>**HRESULT \_ da \_ Win32 (errore \_ dell' \_ handle di monitoraggio non valido \_ )**</dt> </dl> | Il monitoraggio specificato dall'handle di monitoraggio non supporta l'ancoraggio.<br/> |



 

Se *puMaxHeight* o *puFixedWidth* sono null, si verificherà una violazione di accesso.

## <a name="remarks"></a>Commenti

Le finestre di accessibilità possono essere ancorate a un monitor con almeno 768 pixel di schermo verticali. Questa API non consentirà a tali finestre di essere ancorate con un'altezza che comporterebbe la visualizzazione delle app di Windows Store con meno di 768 pixel di schermo verticali.

## <a name="examples"></a>Esempi


```
IAccessibilityDockingService *pDockingService;
HRESULT hr = CoCreateInstance(CLSID_AccessibilityDockingService, CLSCTX_INPROV_SERVER, nullptr, IID_PPV_ARGS(&pDockingService));
if (SUCCEEDED(hr))
{
    UINT uMaxHeight;
    UINT uFixedWidth;

    HMONITOR hMonitor = MonitorFromWindow(_hwndMyApplication, MONITOR_DEFAULTTONULL);
    if (hMonitor != nullptr)
    {
        hr = pDockingService->GetAvailableSize(hMonitor, &uMaxHeight, &uFixedWidth);
    }
}
```



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**IAccessibilityDockingService**](/windows/desktop/api/shobjidl/nn-shobjidl-iaccessibilitydockingservice)
</dt> </dl>

 

 





