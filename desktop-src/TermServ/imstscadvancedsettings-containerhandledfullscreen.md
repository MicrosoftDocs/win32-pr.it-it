---
title: Proprietà ContainerHandledFullScreen di IMsTscAdvancedSettings
description: Specifica se la modalità a schermo intero gestita dal contenitore è abilitata.
ms.assetid: 67679323-4a74-4d91-abd0-607415295f3d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà ContainerHandledFullScreen
- Servizi Desktop remoto proprietà ContainerHandledFullScreen, interfaccia IMsTscAdvancedSettings
- Interfaccia IMsTscAdvancedSettings Servizi Desktop remoto, proprietà ContainerHandledFullScreen
- Servizi Desktop remoto proprietà ContainerHandledFullScreen, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà ContainerHandledFullScreen
- Servizi Desktop remoto proprietà ContainerHandledFullScreen, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà ContainerHandledFullScreen
- Servizi Desktop remoto proprietà ContainerHandledFullScreen, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà ContainerHandledFullScreen
- Servizi Desktop remoto proprietà ContainerHandledFullScreen, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà ContainerHandledFullScreen
- Servizi Desktop remoto proprietà ContainerHandledFullScreen, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà ContainerHandledFullScreen
- Servizi Desktop remoto proprietà ContainerHandledFullScreen, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà ContainerHandledFullScreen
- Servizi Desktop remoto proprietà ContainerHandledFullScreen, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà ContainerHandledFullScreen
- Servizi Desktop remoto proprietà ContainerHandledFullScreen, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà ContainerHandledFullScreen
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.ContainerHandledFullScreen
- IMsTscAdvancedSettings.get_ContainerHandledFullScreen
- IMsTscAdvancedSettings.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.put_ContainerHandledFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7442ce16e2ff30ca2d9b3bd529d37382d1df41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400739"
---
# <a name="imstscadvancedsettingscontainerhandledfullscreen-property"></a>Proprietà IMsTscAdvancedSettings:: ContainerHandledFullScreen

Specifica se la modalità a schermo intero gestita dal contenitore è abilitata.

> [!Note]  
> Il valore della proprietà **ContainerHandledFullScreen** non ha alcun effetto quando il controllo ActiveX Desktop remoto è sicuro per lo scripting e restituisce **\_ false** quando viene effettuato un tentativo di modificare il valore.

 

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_ContainerHandledFullScreen(
  [in]  BOOL ContainerHandledFullScreen
);

HRESULT get_ContainerHandledFullScreen(
  [out] BOOL *pContainerHandledFullScreen
);
```



## <a name="property-value"></a>Valore proprietà

Impostare questo parametro su **true** per abilitare la modalità o un altro valore per disabilitare la modalità.

## <a name="error-codes"></a>Codici di errore

Restituisce **\_ OK** se ha esito positivo. Restituisce **\_ false** se non è supportato.

## <a name="remarks"></a>Commenti

Quando questa modalità è abilitata, il contenitore corrente elabora il passaggio in e fuori dalla modalità schermo intero. Questo metodo deve essere utilizzato solo se il contenitore corrente necessita di un controllo esteso sul comportamento della modalità a schermo intero. Quando questa proprietà è impostata, il controllo non entra o esce dalla modalità a schermo intero in risposta alla combinazione di tasti di scelta rapida della modalità schermo intero (CTRL + ALT + INTERr); vengono invece chiamati gli eventi [**IMsTscAxEvents:: OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md) e [**IMsTscAxEvents:: OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md) . Per ulteriori informazioni su questi eventi, vedere [**IMsTscAxEvents**](imstscaxevents-interface.md) .

La maggior parte delle applicazioni contenitore non dovrà usare la modalità a schermo intero gestita dal contenitore.

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                            |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings è definito come 809945cc-4b3b-4A92-a6b0-dbf9b5f2ef2d<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





