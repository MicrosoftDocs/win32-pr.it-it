---
description: Descrive i parametri di creazione per un dispositivo.
ms.assetid: 7db5ef2b-6894-4113-b726-8b238bb4fb2f
title: D3DDEVICE_CREATION_PARAMETERS struttura (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVICE_CREATION_PARAMETERS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 64b3e13300d6c305d06b6b13db246134cb889cbfc407e4a99c6ae45adbf916e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805020"
---
# <a name="d3ddevice_creation_parameters-structure"></a>Struttura D3DDEVICE \_ CREATION \_ PARAMETERS

Descrive i parametri di creazione per un dispositivo.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DDEVICE_CREATION_PARAMETERS {
  UINT       AdapterOrdinal;
  D3DDEVTYPE DeviceType;
  HWND       hFocusWindow;
  DWORD      BehaviorFlags;
} D3DDEVICE_CREATION_PARAMETERS, *LPD3DDEVICE_CREATION_PARAMETERS;
```



## <a name="members"></a>Members

<dl> <dt>

**AdapterOrdinal**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero ordinale che indica la scheda di visualizzazione. D3DADAPTER \_ DEFAULT è sempre l'adattatore video primario. Usare questo ordinale come parametro Adapter per uno dei [**metodi IDirect3D9.**](/windows/desktop/api) Si noti che istanze diverse di oggetti Direct3D 9.0 possono usare ordinali diversi. Gli adattatori possono entrare o uscire da un sistema quando gli utenti, ad esempio, aggiungono o rimuovono monitor da un sistema a più monitor o quando scambiano a caldo un computer portatile. Di conseguenza, usare questo ordinale solo in un'istanza direct3D 9.0 nota per essere valida, cio' direct3D 9.0 che ha creato questa [**interfaccia IDirect3DDevice9**](/windows/desktop/api) o Direct3D 9.0 restituito da [**GetDirect3D**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdirect3d), come chiamato tramite questa **interfaccia IDirect3DDevice9.**

</dd> <dt>

**DeviceType**
</dt> <dd>

Tipo: **[ **D3DDEVTYPE**](./d3ddevtype.md)**

</dd> <dd>

Membro del [**tipo enumerato D3DDEVTYPE.**](./d3ddevtype.md) Indica la quantità di funzionalità emulate per questo dispositivo. Il valore di questo parametro rispecchia il valore passato alla [**chiamata CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) che ha creato il dispositivo.

</dd> <dt>

**hFocusWindow**
</dt> <dd>

Tipo: **[ **HWND**](../winprog/windows-data-types.md)**

</dd> <dd>

Handle di finestra a cui appartiene lo stato attivo per questo dispositivo Direct3D. Il valore di questo parametro rispecchia il valore passato alla [**chiamata CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) che ha creato il dispositivo.

</dd> <dt>

**BehaviorFlags**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Combinazione di una o più [costanti D3DCREATE](d3dcreate.md) che controllano il comportamento globale del dispositivo. Queste costanti rispecchiano le costanti passate a [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) al momento della creazione del dispositivo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetCreationParameters**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getcreationparameters)
</dt> <dt>

[**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> </dl>

 

 
