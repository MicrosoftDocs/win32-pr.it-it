---
description: Descrive i parametri di creazione per un dispositivo.
ms.assetid: 7db5ef2b-6894-4113-b726-8b238bb4fb2f
title: Struttura D3DDEVICE_CREATION_PARAMETERS (D3D9Types. h)
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
ms.openlocfilehash: 72b2f35f1666ec2095c6ea8f5d5588dc7fd62f2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354474"
---
# <a name="d3ddevice_creation_parameters-structure"></a>Struttura dei parametri di \_ creazione D3DDEVICE \_

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

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero ordinale che indica la scheda di visualizzazione. \_Il valore predefinito di D3DADAPTER è sempre la scheda di visualizzazione principale. Utilizzare questo ordinale come parametro dell'adapter per uno dei metodi [**IDirect3D9**](/windows/desktop/api) . Si noti che diverse istanze di oggetti Direct3D 9,0 possono utilizzare ordinali diversi. Gli adapter possono immettere o lasciare un sistema quando gli utenti, ad esempio, aggiungono o rimuovono i monitoraggi da un sistema a più monitor o quando eseguono lo scambio a caldo di un portatile. Usare quindi questo ordinale solo in un'istanza di Direct3D 9,0 nota come valida, ovvero Direct3D 9,0 che ha creato questa interfaccia [**IDirect3DDevice9**](/windows/desktop/api) o Direct3D 9,0 restituito da [**getdirect3d**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdirect3d), come chiamato tramite questa interfaccia **IDirect3DDevice9** .

</dd> <dt>

**DeviceType**
</dt> <dd>

Tipo: **[ **D3DDEVTYPE**](./d3ddevtype.md)**

</dd> <dd>

Membro del tipo enumerato [**D3DDEVTYPE**](./d3ddevtype.md) . Indica la quantità di funzionalità emulata per questo dispositivo. Il valore di questo parametro rispecchia il valore passato alla chiamata [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) che ha creato il dispositivo.

</dd> <dt>

**hFocusWindow**
</dt> <dd>

Tipo: **[ **HWND**](../winprog/windows-data-types.md)**

</dd> <dd>

Handle di finestra a cui appartiene lo stato attivo per questo dispositivo Direct3D. Il valore di questo parametro rispecchia il valore passato alla chiamata [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) che ha creato il dispositivo.

</dd> <dt>

**BehaviorFlags**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Combinazione di una o più costanti [D3DCREATE](d3dcreate.md) che controllano il comportamento globale del dispositivo. Queste costanti rispecchiano le costanti passate a [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) al momento della creazione del dispositivo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetCreationParameters**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getcreationparameters)
</dt> <dt>

[**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> </dl>

 

 
