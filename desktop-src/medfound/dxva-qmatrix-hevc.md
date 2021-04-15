---
description: Definisce una matrice di quantizzazione.
ms.assetid: 44a5c81f-98d8-4b16-a467-433bae781691
title: Struttura DXVA_Qmatrix_HEVC (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_Qmatrix_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 2aba66636717eee5deb04032d9408ace495e1edf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524546"
---
# <a name="dxva_qmatrix_hevc-structure"></a><span data-ttu-id="025df-103">\_Struttura DXVA Qmatrix \_ HEVC</span><span class="sxs-lookup"><span data-stu-id="025df-103">DXVA\_Qmatrix\_HEVC structure</span></span>

<span data-ttu-id="025df-104">Definisce una matrice di quantizzazione.</span><span class="sxs-lookup"><span data-stu-id="025df-104">Defines a quantization matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="025df-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="025df-105">Syntax</span></span>


```C++
typedef struct _DXVA_Qmatrix_HEVC {
  UCHAR ucScalingLists0[6][16];
  UCHAR ucScalingLists1[6][64];
  UCHAR ucScalingLists2[6][64];
  UCHAR ucScalingLists3[2][64];
  UCHAR ucScalingListDCCoefSizeID2[6];
  UCHAR ucScalingListDCCoefSizeID3[2];
} DXVA_Qmatrix_HEVC, *LPDXVA_Qmatrix_HEVC;
```



## <a name="members"></a><span data-ttu-id="025df-106">Members</span><span class="sxs-lookup"><span data-stu-id="025df-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="025df-107">**ucScalingLists0 \[ 6 \] \[ 16\]**</span><span class="sxs-lookup"><span data-stu-id="025df-107">**ucScalingLists0\[6\]\[16\]**</span></span>
</dt> <dd>

<span data-ttu-id="025df-108">Contiene gli elenchi di ridimensionamento per il processo di ridimensionamento 4x4, corrispondente a \[ \] \[ MatrixID \] \[ i \] nella specifica HEVC, dove MatrixID è compreso nell'intervallo da 0 a 5, inclusivo e i è compreso tra 0 e 15 inclusi.</span><span class="sxs-lookup"><span data-stu-id="025df-108">Contains the scaling lists for the 4x4 scaling process, corresponding to ScalingList\[ 0 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 5, inclusive, and i is in the range of 0 to 15, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="025df-109">**ucScalingLists1 \[ 6 \] \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="025df-109">**ucScalingLists1\[6\]\[64\]**</span></span>
</dt> <dd>

<span data-ttu-id="025df-110">Contiene gli elenchi di ridimensionamento per il processo di ridimensionamento 8x8 Virtual, corrispondente a scalar \[ 1 \] \[ MatrixID \] \[ i \] nella specifica HEVC, dove MatrixID è compreso nell'intervallo da 0 a 5, incluso e i è compreso tra 0 e 63, inclusi.</span><span class="sxs-lookup"><span data-stu-id="025df-110">Contains the scaling lists for the 8x8 scaling process, corresponding to ScalingList\[ 1 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 5, inclusive, and i is in the range of 0 to 63, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="025df-111">**ucScalingLists2 \[ 6 \] \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="025df-111">**ucScalingLists2\[6\]\[64\]**</span></span>
</dt> <dd>

<span data-ttu-id="025df-112">Contiene gli elenchi di ridimensionamento per il processo di ridimensionamento 8x8 Virtual, corrispondente a scalar \[ 2 \] \[ MatrixID \] \[ i \] nella specifica HEVC, dove MatrixID è compreso nell'intervallo da 0 a 5, incluso e i è compreso tra 0 e 63, inclusi.</span><span class="sxs-lookup"><span data-stu-id="025df-112">Contains the scaling lists for the 8x8 scaling process, corresponding to ScalingList\[ 2 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 5, inclusive, and i is in the range of 0 to 63, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="025df-113">**ucScalingLists3 \[ 2 \] \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="025df-113">**ucScalingLists3\[2\]\[64\]**</span></span>
</dt> <dd>

<span data-ttu-id="025df-114">Contiene gli elenchi di ridimensionamento per il processo di ridimensionamento 8x8 Virtual, corrispondenti a scaling \[ 3 \] \[ MatrixID \] \[ i \] nella specifica HEVC, dove MatrixID è compreso nell'intervallo tra 0 e 1, inclusivo e i è compreso tra 0 e 63, inclusi.</span><span class="sxs-lookup"><span data-stu-id="025df-114">Contains the scaling lists for the 8x8 scaling process, corresponding to ScalingList\[ 3 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 1, inclusive, and i is in the range of 0 to 63, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="025df-115">**ucScalingListDCCoefSizeID2**</span><span class="sxs-lookup"><span data-stu-id="025df-115">**ucScalingListDCCoefSizeID2**</span></span>
</dt> <dd>

<span data-ttu-id="025df-116">Contiene il valore del controller di dominio dell'elenco di ridimensionamento per le dimensioni 16x16 con sizeID uguale a 2 e corrispondente all'elenco di ridimensionamento \_ \_ DC \_ coefficiente \_ minus8 \[ sizeID − 2 \] \[ matrixID \] + 8 con sizeID uguale a 2 e matrixID nell'intervallo compreso tra 0 e 5, incluso, nella specifica HEVC.</span><span class="sxs-lookup"><span data-stu-id="025df-116">Contains the DC value of the scaling list for 16x16 size with sizeID equal to 2 and corresponding to scaling\_list\_dc\_coef\_minus8\[ sizeID − 2 \]\[ matrixID \] +8 with sizeID equal to 2 and matrixID in the range of 0 to 5, inclusive, in HEVC specification.</span></span>

</dd> <dt>

<span data-ttu-id="025df-117">**ucScalingListDCCoefSizeID3**</span><span class="sxs-lookup"><span data-stu-id="025df-117">**ucScalingListDCCoefSizeID3**</span></span>
</dt> <dd>

<span data-ttu-id="025df-118">Contiene il valore del controller di dominio dell'elenco di ridimensionamento per le dimensioni di 32x32 con sizeID uguale a 3 e corrispondente all'elenco di ridimensionamento \_ \_ DC \_ coefficiente \_ minus8 \[ sizeID − 2 \] \[ matrixID \] + 8 con sizeID uguale a 3 e matrixID nell'intervallo compreso tra 0 e 1, inclusi, nella specifica HEVC.</span><span class="sxs-lookup"><span data-stu-id="025df-118">Contains the DC value of the scaling list for 32x32 size with sizeID equal to 3, and corresponding to scaling\_list\_dc\_coef\_minus8\[ sizeID − 2 \]\[ matrixID \] +8 with sizeID equal to 3 and matrixID in the range of 0 to 1, inclusive, in HEVC specification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="025df-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="025df-119">Requirements</span></span>



| <span data-ttu-id="025df-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="025df-120">Requirement</span></span> | <span data-ttu-id="025df-121">Valore</span><span class="sxs-lookup"><span data-stu-id="025df-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="025df-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="025df-122">Minimum supported client</span></span><br/> | <span data-ttu-id="025df-123">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="025df-123">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="025df-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="025df-124">Minimum supported server</span></span><br/> | <span data-ttu-id="025df-125">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="025df-125">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="025df-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="025df-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="025df-127"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="025df-127"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="025df-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="025df-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="025df-129">Strutture di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="025df-129">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 




