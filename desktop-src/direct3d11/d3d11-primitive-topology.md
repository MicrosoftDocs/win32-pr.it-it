---
description: Modalità di interpretazione dei dati dei vertici associati alla fase dell'assembler di input. Questi valori di topologia primitiva determinano il modo in cui viene eseguito il rendering dei dati dei vertici sullo schermo.
ms.assetid: ca0547b2-d0f8-4edc-a62c-3c903e1b33ea
title: Enumerazione DELLA TOPOLOGIA PRIMITIVA D3D11 \_ \_
ms.date: 06/26/2019
ms.topic: reference
ms.openlocfilehash: 7c899d738b2a80036eaea61352f5e8aa82c73ddbeb48433d275d74506a478d49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990011"
---
# <a name="d3d11_primitive_topology-enumeration"></a>Enumerazione DELLA TOPOLOGIA PRIMITIVA D3D11 \_ \_

Modalità di interpretazione dei dati dei vertici associati alla fase dell'assembler di input. Questi valori di topologia primitiva determinano il modo in cui viene eseguito il rendering dei dati dei vertici sullo schermo.

## <a name="syntax"></a>Sintassi


```C++
} D3D11_PRIMITIVE_TOPOLOGY;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="d3d11_primitive_topology_undefined"></span>**TOPOLOGIA PRIMITIVA D3D11 \_ \_ NON \_ DEFINITA**
</dt> <dd>

La fase IA non è stata inizializzata con una topologia primitiva. La fase IA non funzionerà correttamente a meno che non venga definita una topologia primitiva.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="d3d11_primitive_topology_pointlist"></span>**POINTLIST DELLA TOPOLOGIA \_ PRIMITIVA D3D11 \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di punti.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="d3d11_primitive_topology_linelist"></span>**ELENCO DI LINEE DELLA TOPOLOGIA PRIMITIVA D3D11 \_ \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di righe.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="d3d11_primitive_topology_linestrip"></span>**LINEA DELLA TOPOLOGIA PRIMITIVA D3D11 \_ \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come una striscia di linee.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="d3d11_primitive_topology_trianglelist"></span>**TRIANGOLO TOPOLOGIA \_ PRIMITIVA D3D11LIST \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di triangoli.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="d3d11_primitive_topology_trianglestrip"></span>**TRIANGOLO DELLA TOPOLOGIA \_ PRIMITIVA D3D11 \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come striscia triangolare.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="d3d11_primitive_topology_linelist_adj"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ LINELIST \_ ADJ**
</dt> <dd>

Interpretare i dati dei vertici come elenco di righe con dati di adicenza.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="d3d11_primitive_topology_linestrip_adj"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ LINESTRIP \_ ADJ**
</dt> <dd>

Interpretare i dati dei vertici come line strip con dati di adicenza.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="d3d11_primitive_topology_trianglelist_adj"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ TRIANGLELIST \_ ADJ**
</dt> <dd>

Interpretare i dati dei vertici come elenco di triangoli con dati di adicenza.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="d3d11_primitive_topology_trianglestrip_adj"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ TRIANGLESTRIP \_ ADJ**
</dt> <dd>

Interpretare i dati dei vertici come striscia triangolare con dati di adicenza.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_1_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 1 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_2_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 2 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_3_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 3 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_4_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 4 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_5_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 5 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_6_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 6 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_7_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 7 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_8_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 8 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_9_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 9 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_10_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 10 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_11_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 11 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_12_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 12 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_13_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 13 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_14_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 14 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_15_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 15 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_16_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 16 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_17_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 17 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_18_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 18 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_19_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 19 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_20_control_point_patchlist"></span>**PATCHLIST DEI PUNTI DI CONTROLLO D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 20 \_ \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_21_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 21 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_22_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 22 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_23_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 23 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_24_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 24 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_25_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 25 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_26_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 26 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_27_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 27 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_28_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 28 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_29_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 29 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_30_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 30 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_31_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 31 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_32_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 32 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interpretare i dati dei vertici come elenco di patch.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'enumerazione **D3D11 \_ PRIMITIVE \_ TOPOLOGY** è un tipo definito nel file di intestazione D3D11.h come enumerazione [**D3D \_ PRIMITIVE \_ TOPOLOGY,**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology) che è completamente definito nel file di intestazione D3DCommon.h.
