---
description: Il metodo DoInitialize deve essere implementato dal monitoraggio. MCSVC chiama questo metodo per ottenere un filtro di acquisizione immediatamente prima di chiamare il metodo IRTCConnect dei criteri di rete.
ms.assetid: 5e43be75-21b3-4f37-ad53-3ffdd55f56a1
title: Metodo IMonitorDoInitialize (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.DoInitialize
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 013a1604c1cbc709f35ac23378bab008d6c67f9053c171190b20669106303f37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779181"
---
# <a name="imonitordoinitialize-method"></a>Metodo IMonitor::D oInitialize

Il **metodo DoInitialize** deve essere implementato dal monitoraggio. MCSVC chiama questo metodo per ottenere un filtro di acquisizione immediatamente prima di chiamare il metodo [IRTC::Connessione](irtc-connect.md) NPP.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DoInitialize(
  [in]      IUnknown *pUnkMonitorCtrl,
  [in, out] HBLOB    hNPPBlob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pUnkMonitorCtrl* \[ Pollici\]
</dt> <dd>

Puntatore [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) passato da MCSVC. Per ottenere un'interfaccia di controllo di monitoraggio supportata, il monitoraggio deve chiamare [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sul puntatore.

</dd> <dt>

*hNPPBlob* \[ in, out\]
</dt> <dd>

Nell'input, handle a un BLOB NPP.

Nell'output, un BLOB NPP che contiene un filtro di acquisizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è S \_ OK (uguale a NOERROR).

Se il metodo ha esito negativo, il valore restituito è un codice di errore. In caso di errore, MCSVC non creerà il monitoraggio né chiamerà [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sul puntatore di interfaccia.

## <a name="remarks"></a>Commenti

MCSVC chiama il metodo **DoInitialize** per eseguire l'inizializzazione del monitoraggio necessaria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

