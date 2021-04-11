---
description: Fornisce i parametri a livello di immagine di un'immagine compressa per la decodifica video HEVC.
ms.assetid: F73AE9CD-5BBC-4A9F-8D05-707AD5E2E92A
title: Struttura DXVA_PicParams_HEVC (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_PicParams_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: cafcbf31a7d4b7fee84e6c695f1d0f0a1e0302ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127898"
---
# <a name="dxva_picparams_hevc-structure"></a><span data-ttu-id="54003-103">\_Struttura DXVA PicParams \_ HEVC</span><span class="sxs-lookup"><span data-stu-id="54003-103">DXVA\_PicParams\_HEVC structure</span></span>

<span data-ttu-id="54003-104">Fornisce i parametri a livello di immagine di un'immagine compressa per la decodifica video HEVC.</span><span class="sxs-lookup"><span data-stu-id="54003-104">Provides the picture-level parameters of a compressed picture for HEVC video decoding.</span></span>

## <a name="syntax"></a><span data-ttu-id="54003-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54003-105">Syntax</span></span>


```C++
typedef struct _DXVA_PicParams_HEVC {
  USHORT             PicWidthInMinCbsY;
  USHORT             PicHeightInMinCbsY;
  union {
    struct {
      USHORT chroma_format_idc  :2;
      USHORT separate_colour_plane_flag   :1;
      USHORT bit_depth_luma_minus8   :3;
      USHORT bit_depth_chroma_minus8  :3;
      USHORT log2_max_pic_order_cnt_lsb_minus4  :4;
      USHORT NoPicReorderingFlag   :1;
      USHORT  NoBiPredFlag   :1;
      USHORT ReservedBits1     :1;
    };
    USHORT  wFormatAndSequenceInfoFlags;
  };
  DXVA_PicEntry_HEVC CurrPic;
  UCHAR              sps_max_dec_pic_buffering_minus1;
  UCHAR              log2_min_luma_coding_block_size_minus3;
  UCHAR              log2_diff_max_min_luma_coding_block_size;
  UCHAR              log2_min_transform_block_size_minus2;
  UCHAR              log2_diff_max_min_transform_block_size;
  UCHAR              max_transform_hierarchy_depth_inter;
  UCHAR              max_transform_hierarchy_depth_intra;
  UCHAR              num_short_term_ref_pic_sets;
  UCHAR              num_long_term_ref_pics_sps;
  UCHAR              num_ref_idx_l0_default_active_minus1;
  UCHAR              num_ref_idx_l1_default_active_minus1;
  CHAR               init_qp_minus26;
  UCHAR              ucNumDeltaPocsOfRefRpsIdx;
  USHORT             wNumBitsForShortTermRPSInSlice;
  USHORT             ReservedBits2;
  union {
    struct {
      UINT32 scaling_list_enabled_flag  :1;
      UINT32 amp_enabled_flag  :1;
      UINT32 sample_adaptive_offset_enabled_flag  :1;
      UINT32 pcm_enabled_flag   :1;
      UINT32 pcm_sample_bit_depth_luma_minus1   :4;
      UINT32 pcm_sample_bit_depth_chroma_minus1     :4;
      UINT32 log2_min_pcm_luma_coding_block_size_minus3    :2;
      UINT32 log2_diff_max_min_pcm_luma_coding_block_size  :2;
      UINT32 pcm_loop_filter_disabled_flag  :1;
      UINT32 long_term_ref_pics_present_flag   :1;
      UINT32 sps_temporal_mvp_enabled_flag  :1;
      UINT32 strong_intra_smoothing_enabled_flag   :1;
      UINT32 dependent_slice_segments_enabled_flag    :1;
      UINT32 output_flag_present_flag   :1;
      UINT32 num_extra_slice_header_bits    :3;
      UINT32 sign_data_hiding_enabled_flag  :1;
      UINT32 cabac_init_present_flag  :1;
      UINT32 ReservedBits3    :5;
    };
    UINT32             dwCodingParamToolFlags;
    union {
      struct {
        UINT32 constrained_intra_pred_flag  :1;
        UINT32 transform_skip_enabled_flag  :1;
        UINT32 cu_qp_delta_enabled_flag  :1;
        UINT32 pps_slice_chroma_qp_offsets_present_flag  :1;
        UINT32 weighted_pred_flag  :1;
        UINT32 weighted_bipred_flag  :1;
        UINT32 transquant_bypass_enabled_flag  :1;
        UINT32 tiles_enabled_flag   :1;
        UINT32 entropy_coding_sync_enabled_flag   :1;
        UINT32 uniform_spacing_flag    :1;
        UINT32 loop_filter_across_tiles_enabled_flag   :1;
        UINT32 pps_loop_filter_across_slices_enabled_flag  :1;
        UINT32 deblocking_filter_override_enabled_flag  :1;
        UINT32 pps_deblocking_filter_disabled_flag  :1;
        UINT32 lists_modification_present_flag  :1;
        UINT32 slice_segment_header_extension_present_flag  :1;
        UINT32 IrapPicFlag  :1;
        UINT32 IdrPicFlag     :1;
        UINT32 IntraPicFlag   :1;
        UINT32 ReservedBits4     :13;
      };
      UINT32   dwCodingSettingPicturePropertyFlags;
    };
    CHAR               pps_cb_qp_offset;
    CHAR               pps_cr_qp_offset;
    UCHAR              num_tile_columns_minus1;
    UCHAR              num_tile_rows_minus1;
    USHORT             column_width_minus1[19];
    USHORT             row_height_minus1[21];
    UCHAR              diff_cu_qp_delta_depth;
    CHAR               pps_beta_offset_div2;
    CHAR               pps_tc_offset_div2;
    UCHAR              log2_parallel_merge_level_minus2;
    INT                CurrPicOrderCntVal;
    DXVA_PicEntry_HEVC RefPicList[15];
    UCHAR              ReservedBits5;
    INT                PicOrderCntValList[15];
    UCHAR              RefPicSetStCurrBefore[8];
    UCHAR              RefPicSetStCurrAfter[8];
    UCHAR              RefPicSetLtCurr[8];
    USHORT             ReservedBits6;
    USHORT             ReservedBits7;
    UINT               StatusReportFeedbackNumber;
  };
} DXVA_PicParams_HEVC, *PDXVA_PicParams_HEVC;
```



## <a name="members"></a><span data-ttu-id="54003-106">Members</span><span class="sxs-lookup"><span data-stu-id="54003-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="54003-107">**PicWidthInMinCbsY**</span><span class="sxs-lookup"><span data-stu-id="54003-107">**PicWidthInMinCbsY**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-108">**PicHeightInMinCbsY**</span><span class="sxs-lookup"><span data-stu-id="54003-108">**PicHeightInMinCbsY**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-109">**\_formato Chroma \_**</span><span class="sxs-lookup"><span data-stu-id="54003-109">**chroma\_format\_idc**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-110">**\_ \_ flag piano colori \_ separato**</span><span class="sxs-lookup"><span data-stu-id="54003-110">**separate\_colour\_plane\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-111">**\_ \_ minus8 luminanza bit profondità \_**</span><span class="sxs-lookup"><span data-stu-id="54003-111">**bit\_depth\_luma\_minus8**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-112">**profondità di bit \_ \_ Chroma \_ minus8**</span><span class="sxs-lookup"><span data-stu-id="54003-112">**bit\_depth\_chroma\_minus8**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-113">**log2 \_ Max \_ pic \_ Order \_ CNT \_ LSB \_ minus4**</span><span class="sxs-lookup"><span data-stu-id="54003-113">**log2\_max\_pic\_order\_cnt\_lsb\_minus4**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-114">**NoPicReorderingFlag**</span><span class="sxs-lookup"><span data-stu-id="54003-114">**NoPicReorderingFlag**</span></span> 
</dt> <dd></dd> <dt>

 <span data-ttu-id="54003-115">**NoBiPredFlag**</span><span class="sxs-lookup"><span data-stu-id="54003-115">**NoBiPredFlag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-116">**ReservedBits1**</span><span class="sxs-lookup"><span data-stu-id="54003-116">**ReservedBits1**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-117">**wFormatAndSequenceInfoFlags**</span><span class="sxs-lookup"><span data-stu-id="54003-117">**wFormatAndSequenceInfoFlags**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-118">**CurrPic**</span><span class="sxs-lookup"><span data-stu-id="54003-118">**CurrPic**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-119">**\_numero massimo \_ Dec \_ pic \_ buffering \_ Minus1**</span><span class="sxs-lookup"><span data-stu-id="54003-119">**sps\_max\_dec\_pic\_buffering\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-120">**\_dimensioni del \_ blocco del codice Luma minimo log2 \_ \_ \_ \_ minus3**</span><span class="sxs-lookup"><span data-stu-id="54003-120">**log2\_min\_luma\_coding\_block\_size\_minus3**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-121">**\_dimensioni del \_ \_ blocco di \_ \_ codice Luma \_ minimo \_ log2 diff**</span><span class="sxs-lookup"><span data-stu-id="54003-121">**log2\_diff\_max\_min\_luma\_coding\_block\_size**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-122">**\_dimensioni del \_ blocco di trasformazione log2 min \_ \_ \_ Minus2**</span><span class="sxs-lookup"><span data-stu-id="54003-122">**log2\_min\_transform\_block\_size\_minus2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-123">**\_dimensioni del \_ \_ blocco di \_ trasformazione \_ minimo log2 diff Max \_**</span><span class="sxs-lookup"><span data-stu-id="54003-123">**log2\_diff\_max\_min\_transform\_block\_size**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-124">**massimo \_ \_ profondità gerarchia di trasformazione \_ \_ tra**</span><span class="sxs-lookup"><span data-stu-id="54003-124">**max\_transform\_hierarchy\_depth\_inter**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-125">**\_profondità massima \_ gerarchia di trasformazione \_ \_ intra**</span><span class="sxs-lookup"><span data-stu-id="54003-125">**max\_transform\_hierarchy\_depth\_intra**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-126">**numeri a \_ breve \_ termine per \_ \_ set di pic Ref \_**</span><span class="sxs-lookup"><span data-stu-id="54003-126">**num\_short\_term\_ref\_pic\_sets**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-127">**num \_ \_ pics ref a lungo termine \_ \_ \_ SPS**</span><span class="sxs-lookup"><span data-stu-id="54003-127">**num\_long\_term\_ref\_pics\_sps**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-128">**num \_ ref \_ idx \_ L0 \_ default \_ Active \_ Minus1**</span><span class="sxs-lookup"><span data-stu-id="54003-128">**num\_ref\_idx\_l0\_default\_active\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-129">**num \_ ref \_ idx \_ L1 \_ default \_ Active \_ Minus1**</span><span class="sxs-lookup"><span data-stu-id="54003-129">**num\_ref\_idx\_l1\_default\_active\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-130">**init \_ QP \_ minus26**</span><span class="sxs-lookup"><span data-stu-id="54003-130">**init\_qp\_minus26**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-131">**ucNumDeltaPocsOfRefRpsIdx**</span><span class="sxs-lookup"><span data-stu-id="54003-131">**ucNumDeltaPocsOfRefRpsIdx**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-132">**wNumBitsForShortTermRPSInSlice**</span><span class="sxs-lookup"><span data-stu-id="54003-132">**wNumBitsForShortTermRPSInSlice**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-133">**ReservedBits2**</span><span class="sxs-lookup"><span data-stu-id="54003-133">**ReservedBits2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-134">**flag di ridimensionamento \_ elenco \_ abilitato \_**</span><span class="sxs-lookup"><span data-stu-id="54003-134">**scaling\_list\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-135">**\_flag di abilitazione amp \_**</span><span class="sxs-lookup"><span data-stu-id="54003-135">**amp\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-136">**flag di esempio \_ Adaptive \_ offset \_ abilitato \_**</span><span class="sxs-lookup"><span data-stu-id="54003-136">**sample\_adaptive\_offset\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-137">**\_flag abilitato \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="54003-137">**pcm\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-138">**\_Minus1 di \_ profondità del bit di esempio PCM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="54003-138">**pcm\_sample\_bit\_depth\_luma\_minus1**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-139">**profondità del bit di esempio del PCM \_ \_ \_ \_ \_ Minus1 Chroma**</span><span class="sxs-lookup"><span data-stu-id="54003-139">**pcm\_sample\_bit\_depth\_chroma\_minus1**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-140">**\_ \_ \_ \_ dimensioni blocco codifica Luma log2 min PCM \_ \_ \_ minus3**</span><span class="sxs-lookup"><span data-stu-id="54003-140">**log2\_min\_pcm\_luma\_coding\_block\_size\_minus3**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-141">**\_dimensioni del \_ \_ blocco di \_ \_ codifica Luma \_ \_ max min \_ PCM log2**</span><span class="sxs-lookup"><span data-stu-id="54003-141">**log2\_diff\_max\_min\_pcm\_luma\_coding\_block\_size**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-142">**\_flag di \_ filtro ciclo PCM \_ disabilitato \_**</span><span class="sxs-lookup"><span data-stu-id="54003-142">**pcm\_loop\_filter\_disabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-143">**\_ \_ \_ \_ flag present pics ref \_ a lungo termine**</span><span class="sxs-lookup"><span data-stu-id="54003-143">**long\_term\_ref\_pics\_present\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-144">**\_flag di \_ \_ Abilitazione del MVP temporale SPS \_**</span><span class="sxs-lookup"><span data-stu-id="54003-144">**sps\_temporal\_mvp\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-145">**\_flag Strong intra \_ smoothing \_ abilitato \_**</span><span class="sxs-lookup"><span data-stu-id="54003-145">**strong\_intra\_smoothing\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-146">**\_flag per segmenti di sezione dipendenti \_ \_ abilitato \_**</span><span class="sxs-lookup"><span data-stu-id="54003-146">**dependent\_slice\_segments\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-147">**flag di output \_ flag \_ presente \_**</span><span class="sxs-lookup"><span data-stu-id="54003-147">**output\_flag\_present\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-148">**numero \_ di \_ \_ bit di intestazione di sezione aggiuntivi \_**</span><span class="sxs-lookup"><span data-stu-id="54003-148">**num\_extra\_slice\_header\_bits**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-149">**\_flag di \_ \_ Abilitazione Nascondi dati \_ firma**</span><span class="sxs-lookup"><span data-stu-id="54003-149">**sign\_data\_hiding\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-150">**\_flag CABAC init \_ present \_**</span><span class="sxs-lookup"><span data-stu-id="54003-150">**cabac\_init\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-151">**ReservedBits3**</span><span class="sxs-lookup"><span data-stu-id="54003-151">**ReservedBits3**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-152">**dwCodingParamToolFlags**</span><span class="sxs-lookup"><span data-stu-id="54003-152">**dwCodingParamToolFlags**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-153">**\_ \_ flag di indazione intra vincolato \_**</span><span class="sxs-lookup"><span data-stu-id="54003-153">**constrained\_intra\_pred\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-154">**\_flag di \_ Abilitazione della trasformazione ignora \_**</span><span class="sxs-lookup"><span data-stu-id="54003-154">**transform\_skip\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-155">**\_flag di \_ \_ Abilitazione \_ Delta di cu QP**</span><span class="sxs-lookup"><span data-stu-id="54003-155">**cu\_qp\_delta\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-156">**\_flag di \_ cromatura della sezione \_ \_ PPS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="54003-156">**pps\_slice\_chroma\_qp\_offsets\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-157">**\_flag prede ponderato \_**</span><span class="sxs-lookup"><span data-stu-id="54003-157">**weighted\_pred\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-158">**\_flag bipredator ponderato \_**</span><span class="sxs-lookup"><span data-stu-id="54003-158">**weighted\_bipred\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-159">**\_ \_ flag di abilitazione bypass di transquant \_**</span><span class="sxs-lookup"><span data-stu-id="54003-159">**transquant\_bypass\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-160">**\_flag abilitati riquadri \_**</span><span class="sxs-lookup"><span data-stu-id="54003-160">**tiles\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-161">**\_flag di sincronizzazione del codice entropia \_ \_ abilitato \_**</span><span class="sxs-lookup"><span data-stu-id="54003-161">**entropy\_coding\_sync\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-162">**\_flag di spaziatura uniforme \_**</span><span class="sxs-lookup"><span data-stu-id="54003-162">**uniform\_spacing\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-163">**\_flag ciclo \_ tra \_ riquadri \_ abilitati \_**</span><span class="sxs-lookup"><span data-stu-id="54003-163">**loop\_filter\_across\_tiles\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-164">**\_filtro ciclo \_ PPS \_ tra le \_ sezioni \_ abilitate \_ flag**</span><span class="sxs-lookup"><span data-stu-id="54003-164">**pps\_loop\_filter\_across\_slices\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-165">**flag di deblocking \_ \_ abilitato per l'override del filtro \_ \_**</span><span class="sxs-lookup"><span data-stu-id="54003-165">**deblocking\_filter\_override\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-166">**\_flag di deblocco del filtro di PPS \_ \_ disabilitato \_**</span><span class="sxs-lookup"><span data-stu-id="54003-166">**pps\_deblocking\_filter\_disabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-167">**\_ \_ flag presente elenco \_ modifiche**</span><span class="sxs-lookup"><span data-stu-id="54003-167">**lists\_modification\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-168">**\_ \_ \_ \_ flag presente estensione intestazione segmento di sezione \_**</span><span class="sxs-lookup"><span data-stu-id="54003-168">**slice\_segment\_header\_extension\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-169">**IrapPicFlag**</span><span class="sxs-lookup"><span data-stu-id="54003-169">**IrapPicFlag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-170">**IdrPicFlag**</span><span class="sxs-lookup"><span data-stu-id="54003-170">**IdrPicFlag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-171">**IntraPicFlag**</span><span class="sxs-lookup"><span data-stu-id="54003-171">**IntraPicFlag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-172">**ReservedBits4**</span><span class="sxs-lookup"><span data-stu-id="54003-172">**ReservedBits4**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-173">**dwCodingSettingPicturePropertyFlags**</span><span class="sxs-lookup"><span data-stu-id="54003-173">**dwCodingSettingPicturePropertyFlags**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-174">**\_ \_ offset QP CB \_ PPS**</span><span class="sxs-lookup"><span data-stu-id="54003-174">**pps\_cb\_qp\_offset**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-175">**\_offset CR \_ QP di PPS \_**</span><span class="sxs-lookup"><span data-stu-id="54003-175">**pps\_cr\_qp\_offset**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-176">**num \_ \_ colonne riquadro \_ Minus1**</span><span class="sxs-lookup"><span data-stu-id="54003-176">**num\_tile\_columns\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-177">**numero \_ di \_ righe del riquadro \_ Minus1**</span><span class="sxs-lookup"><span data-stu-id="54003-177">**num\_tile\_rows\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-178">**\_Minus1 larghezza \_ colonna**</span><span class="sxs-lookup"><span data-stu-id="54003-178">**column\_width\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-179">**\_altezza riga \_ Minus1**</span><span class="sxs-lookup"><span data-stu-id="54003-179">**row\_height\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-180">**\_ \_ \_ profondità Delta QP diff \_ cu**</span><span class="sxs-lookup"><span data-stu-id="54003-180">**diff\_cu\_qp\_delta\_depth**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-181">**\_offset beta di PPS \_ \_ div2**</span><span class="sxs-lookup"><span data-stu-id="54003-181">**pps\_beta\_offset\_div2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-182">**\_offset TC \_ PPS \_ div2**</span><span class="sxs-lookup"><span data-stu-id="54003-182">**pps\_tc\_offset\_div2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-183">**log2 \_ a \_ livello di merge parallelo \_ \_ Minus2**</span><span class="sxs-lookup"><span data-stu-id="54003-183">**log2\_parallel\_merge\_level\_minus2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-184">**CurrPicOrderCntVal**</span><span class="sxs-lookup"><span data-stu-id="54003-184">**CurrPicOrderCntVal**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-185">**RefPicList**</span><span class="sxs-lookup"><span data-stu-id="54003-185">**RefPicList**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-186">**ReservedBits5**</span><span class="sxs-lookup"><span data-stu-id="54003-186">**ReservedBits5**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-187">**PicOrderCntValList**</span><span class="sxs-lookup"><span data-stu-id="54003-187">**PicOrderCntValList**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-188">**RefPicSetStCurrBefore**</span><span class="sxs-lookup"><span data-stu-id="54003-188">**RefPicSetStCurrBefore**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-189">**RefPicSetStCurrAfter**</span><span class="sxs-lookup"><span data-stu-id="54003-189">**RefPicSetStCurrAfter**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-190">**RefPicSetLtCurr**</span><span class="sxs-lookup"><span data-stu-id="54003-190">**RefPicSetLtCurr**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-191">**ReservedBits6**</span><span class="sxs-lookup"><span data-stu-id="54003-191">**ReservedBits6**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-192">**ReservedBits7**</span><span class="sxs-lookup"><span data-stu-id="54003-192">**ReservedBits7**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="54003-193">**StatusReportFeedbackNumber**</span><span class="sxs-lookup"><span data-stu-id="54003-193">**StatusReportFeedbackNumber**</span></span>
<span data-ttu-id="54003-194"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="54003-194"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="54003-195">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54003-195">Requirements</span></span>



| <span data-ttu-id="54003-196">Requisito</span><span class="sxs-lookup"><span data-stu-id="54003-196">Requirement</span></span> | <span data-ttu-id="54003-197">Valore</span><span class="sxs-lookup"><span data-stu-id="54003-197">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="54003-198">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54003-198">Minimum supported client</span></span><br/> | <span data-ttu-id="54003-199">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="54003-199">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="54003-200">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54003-200">Minimum supported server</span></span><br/> | <span data-ttu-id="54003-201">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="54003-201">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="54003-202">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54003-202">Header</span></span><br/>                   | <dl> <span data-ttu-id="54003-203"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="54003-203"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54003-204">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54003-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54003-205">Strutture di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="54003-205">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 




