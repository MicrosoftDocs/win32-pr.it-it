---
description: Il metodo DoInitialize deve essere implementato dal monitoraggio. MCSVC chiama questo metodo per ottenere un filtro di acquisizione immediatamente prima di chiamare il metodo IRTCConnect di centrali.
ms.assetid: 5e43be75-21b3-4f37-ad53-3ffdd55f56a1
title: Metodo IMonitorDoInitialize (Netmon. h)
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
ms.openlocfilehash: 93133ce8204e49d080f87635ad6952685f2ba82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525116"
---
# <a name="imonitordoinitialize-method"></a>IMonitor::D Metodo oInitialize

Il metodo **DoInitialize** deve essere implementato dal monitoraggio. MCSVC chiama questo metodo per ottenere un filtro di acquisizione immediatamente prima di chiamare il metodo [IRTC:: Connect](irtc-connect.md) di NPP.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DoInitialize(
  [in]      IUnknown *pUnkMonitorCtrl,
  [in, out] HBLOB    hNPPBlob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pUnkMonitorCtrl* \[ in\]
</dt> <dd>

Puntatore [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) passato da MCSVC. Per ottenere un'interfaccia di controllo di monitoraggio supportata, il monitoraggio deve chiamare [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sull'indicatore di misura.

</dd> <dt>

*hNPPBlob* \[ in uscita\]
</dt> <dd>

In input, un handle per un BLOB di NPP.

Nell'output, un BLOB di NPP che contiene un filtro di acquisizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è \_ OK (che corrisponde a NOERROR).

Se il metodo ha esito negativo, il valore restituito è un codice di errore. In errore, MCSVC non creerà il monitoraggio o chiamerà [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sul puntatore a interfaccia.

## <a name="remarks"></a>Commenti

MCSVC chiama il metodo **DoInitialize** per eseguire l'inizializzazione del monitoraggio richiesta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

