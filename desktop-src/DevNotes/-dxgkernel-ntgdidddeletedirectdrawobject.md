---
description: Elimina un oggetto dispositivo Microsoft DirectDraw in modalità kernel creato in precedenza.
ms.assetid: 0b2e1bae-8291-4fe4-9528-980680906e0a
title: Funzione NtGdiDdDeleteDirectDrawObject (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDeleteDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 866624e35c5c05afa14692a2e83d1c15293af9435aa68deddf9c602b80820708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956550"
---
# <a name="ntgdidddeletedirectdrawobject-function"></a>Funzione NtGdiDdDeleteDirectDrawObject

\[Questa funzione è soggetta a modifiche con ogni revisione del sistema operativo. Usare invece DirectDraw e Microsoft Direct3DAPIs. Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà nell'interazione diretta con i driver di visualizzazione.\]

Elimina un oggetto dispositivo Microsoft DirectDraw in modalità kernel creato in precedenza.

## <a name="syntax"></a>Sintassi


```C++
BOOL APIENTRY NtGdiDdDeleteDirectDrawObject(
   HANDLE hDirectDrawLocal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDirectDrawLocal* 
</dt> <dd>

Handle per l'oggetto dispositivo DirectDraw in modalità kernel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, questa funzione restituisce **TRUE;** In caso contrario, **restituisce FALSE.**

## <a name="remarks"></a>Commenti

È consigliabile che le applicazioni usino le API DirectDraw e [Direct3D](../direct3d10/d3d10-graphics-reference.md) per creare e gestire oggetti dispositivo grafico. Questi costrutti astrarno il processo di creazione del dispositivo in modo semplificato e indipendente dal sistema operativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto client di basso livello per grafica](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> <dt>

[**DdDeleteDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-dddeletedirectdrawobject)
</dt> </dl>

 

 
