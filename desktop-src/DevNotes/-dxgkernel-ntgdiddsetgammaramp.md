---
description: Imposta la rampa gamma per il dispositivo.
ms.assetid: 92ea0247-6eec-4c5f-9ea7-65f6b97dde1e
title: Funzione NtGdiDdSetGammaRamp (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetGammaRamp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 0c5efba67eedbd6e70f1e0682f42c1855948cecd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125931"
---
# <a name="ntgdiddsetgammaramp-function"></a>NtGdiDdSetGammaRamp (funzione)

\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo. Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]

Imposta la rampa gamma per il dispositivo.

## <a name="syntax"></a>Sintassi


```C++
BOOL APIENTRY NtGdiDdSetGammaRamp(
  _In_ HANDLE hDirectDraw,
  _In_ HDC    hdc,
  _In_ LPVOID lpGammaRamp
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDirectDraw* \[ in\]
</dt> <dd>

Handle per l'oggetto driver in modalità kernel per il quale è necessario impostare la rampa.

</dd> <dt>

*HDC* \[ in\]
</dt> <dd>

Riservato.

</dd> <dt>

*lpGammaRamp* \[ in\]
</dt> <dd>

Puntatore a una matrice di strutture **DDGAMMARAMP** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **true** se la funzione ha esito positivo. In caso contrario, è **null**.

## <a name="remarks"></a>Commenti

È consigliabile che le applicazioni usino invece i metodi **IDirectDrawGammaControl:: SetGammaRamp** o [**IDirect3DDevice9:: SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) , perché questi metodi offrono la stessa funzionalità indipendentemente dal sistema operativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto client di livello inferiore grafica](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
