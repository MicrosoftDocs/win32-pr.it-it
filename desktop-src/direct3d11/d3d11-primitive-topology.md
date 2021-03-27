---
description: Il modo in cui la pipeline interpreta i dati dei vertici associati alla fase input-assembler. Questi valori di topologia primitivi determinano il rendering dei dati dei vertici sullo schermo.
ms.assetid: ca0547b2-d0f8-4edc-a62c-3c903e1b33ea
title: '\_Enumerazione della \_ topologia PRIMItiva d3d11'
ms.date: 06/26/2019
ms.topic: reference
ms.openlocfilehash: 1d2beab107a3f3abe03e5a17f068e1b508422241
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104995269"
---
# <a name="d3d11_primitive_topology-enumeration"></a>\_Enumerazione della \_ topologia PRIMItiva d3d11

Il modo in cui la pipeline interpreta i dati dei vertici associati alla fase input-assembler. Questi valori di topologia primitivi determinano il rendering dei dati dei vertici sullo schermo.

## <a name="syntax"></a>Sintassi


```C++
} D3D11_PRIMITIVE_TOPOLOGY;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="d3d11_primitive_topology_undefined"></span>**\_Topologia primitiva d3d11 non \_ \_ definita**
</dt> <dd>

La fase IA non è stata inizializzata con una topologia primitiva. La fase IA non funzionerà correttamente a meno che non sia stata definita una topologia primitiva.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="d3d11_primitive_topology_pointlist"></span>**D3D11 \_ della \_ topologia primitiva \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di punti.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="d3d11_primitive_topology_linelist"></span>**\_Linea di \_ topologia PRIMItiva d3d11 \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di righe.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="d3d11_primitive_topology_linestrip"></span>**D3D11 \_ \_ topologia primitiva \_ LINESTRIP**
</dt> <dd>

Interpretare i dati dei vertici come una striscia di linea.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="d3d11_primitive_topology_trianglelist"></span>**Triangolo della \_ \_ topologia PRIMItiva d3d11 \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di triangoli.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="d3d11_primitive_topology_trianglestrip"></span>**D3D11 \_ \_ topologia primitiva \_ TRIANGLESTRIP**
</dt> <dd>

Interpretare i dati dei vertici come una striscia di triangolo.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="d3d11_primitive_topology_linelist_adj"></span>**D3D11 \_ la \_ topologia primitiva di \_ linea \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di righe con dati adiacenza.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="d3d11_primitive_topology_linestrip_adj"></span>**D3D11 \_ \_ topologia primitiva \_ LINESTRIP \_ ADJ**
</dt> <dd>

Interpretare i dati dei vertici come striping con i dati adiacenza.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="d3d11_primitive_topology_trianglelist_adj"></span>**D3D11 \_ \_ triangolico topologia primitive \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di triangoli con dati adiacenza.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="d3d11_primitive_topology_trianglestrip_adj"></span>**D3D11 \_ \_ topologia primitiva \_ TRIANGLESTRIP \_ ADJ**
</dt> <dd>

Interpretare i dati dei vertici come strisce di triangolo con i dati adiacenza.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_1_control_point_patchlist"></span>**D3D11 \_ primitive \_ topologia \_ 1 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_2_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 2 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_3_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 3 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_4_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 4 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_5_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 5 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_6_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 6 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_7_control_point_patchlist"></span>**\_Patch del \_ punto di controllo della topologia primitiva d3d11 \_ 7 \_ \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_8_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitive \_ 8 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_9_control_point_patchlist"></span>**D3D11 \_ \_ punto di controllo topologia primitiva \_ 9 \_ \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_10_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 10 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_11_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 11 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_12_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitive \_ 12 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_13_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitive \_ 13 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_14_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitive \_ 14 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_15_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitive \_ 15 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_16_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 16 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_17_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 17 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_18_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 18 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_19_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitive \_ 19 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_20_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 20 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_21_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 21 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_22_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 22 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_23_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 23 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_24_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitive \_ 24 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_25_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 25 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_26_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 26 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_27_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 27 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_28_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 28 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_29_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 29 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_30_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 30 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_31_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitiva \_ 31 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_32_control_point_patchlist"></span>**D3D11 \_ \_ topologia primitive \_ 32 \_ punto di controllo \_ \_**
</dt> <dd>

Interpretare i dati dei vertici come un elenco di patch.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'enumerazione della **\_ \_ topologia primitiva d3d11** è definita nel file di intestazione d3d11. h come enumerazione di [**\_ \_ topologia primitiva D3D**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology) , completamente definita nel file di intestazione D3DCommon. h.
