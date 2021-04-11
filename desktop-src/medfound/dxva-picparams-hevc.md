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
# <a name="dxva_picparams_hevc-structure"></a>\_Struttura DXVA PicParams \_ HEVC

Fornisce i parametri a livello di immagine di un'immagine compressa per la decodifica video HEVC.

## <a name="syntax"></a>Sintassi


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



## <a name="members"></a>Members

<dl> <dt>

**PicWidthInMinCbsY**
</dt> <dd></dd> <dt>

**PicHeightInMinCbsY**
</dt> <dd></dd> <dt>

**\_formato Chroma \_**
</dt> <dd></dd> <dt>

**\_ \_ flag piano colori \_ separato** 
</dt> <dd></dd> <dt>

**\_ \_ minus8 luminanza bit profondità \_** 
</dt> <dd></dd> <dt>

**profondità di bit \_ \_ Chroma \_ minus8**
</dt> <dd></dd> <dt>

**log2 \_ Max \_ pic \_ Order \_ CNT \_ LSB \_ minus4**
</dt> <dd></dd> <dt>

**NoPicReorderingFlag** 
</dt> <dd></dd> <dt>

 **NoBiPredFlag** 
</dt> <dd></dd> <dt>

**ReservedBits1** 
</dt> <dd></dd> <dt>

**wFormatAndSequenceInfoFlags**
</dt> <dd></dd> <dt>

**CurrPic**
</dt> <dd></dd> <dt>

**\_numero massimo \_ Dec \_ pic \_ buffering \_ Minus1**
</dt> <dd></dd> <dt>

**\_dimensioni del \_ blocco del codice Luma minimo log2 \_ \_ \_ \_ minus3**
</dt> <dd></dd> <dt>

**\_dimensioni del \_ \_ blocco di \_ \_ codice Luma \_ minimo \_ log2 diff**
</dt> <dd></dd> <dt>

**\_dimensioni del \_ blocco di trasformazione log2 min \_ \_ \_ Minus2**
</dt> <dd></dd> <dt>

**\_dimensioni del \_ \_ blocco di \_ trasformazione \_ minimo log2 diff Max \_**
</dt> <dd></dd> <dt>

**massimo \_ \_ profondità gerarchia di trasformazione \_ \_ tra**
</dt> <dd></dd> <dt>

**\_profondità massima \_ gerarchia di trasformazione \_ \_ intra**
</dt> <dd></dd> <dt>

**numeri a \_ breve \_ termine per \_ \_ set di pic Ref \_**
</dt> <dd></dd> <dt>

**num \_ \_ pics ref a lungo termine \_ \_ \_ SPS**
</dt> <dd></dd> <dt>

**num \_ ref \_ idx \_ L0 \_ default \_ Active \_ Minus1**
</dt> <dd></dd> <dt>

**num \_ ref \_ idx \_ L1 \_ default \_ Active \_ Minus1**
</dt> <dd></dd> <dt>

**init \_ QP \_ minus26**
</dt> <dd></dd> <dt>

**ucNumDeltaPocsOfRefRpsIdx**
</dt> <dd></dd> <dt>

**wNumBitsForShortTermRPSInSlice**
</dt> <dd></dd> <dt>

**ReservedBits2**
</dt> <dd></dd> <dt>

**flag di ridimensionamento \_ elenco \_ abilitato \_**
</dt> <dd></dd> <dt>

**\_flag di abilitazione amp \_**
</dt> <dd></dd> <dt>

**flag di esempio \_ Adaptive \_ offset \_ abilitato \_**
</dt> <dd></dd> <dt>

**\_flag abilitato \_ PCM** 
</dt> <dd></dd> <dt>

**\_Minus1 di \_ profondità del bit di esempio PCM \_ \_ \_** 
</dt> <dd></dd> <dt>

**profondità del bit di esempio del PCM \_ \_ \_ \_ \_ Minus1 Chroma** 
</dt> <dd></dd> <dt>

**\_ \_ \_ \_ dimensioni blocco codifica Luma log2 min PCM \_ \_ \_ minus3** 
</dt> <dd></dd> <dt>

**\_dimensioni del \_ \_ blocco di \_ \_ codifica Luma \_ \_ max min \_ PCM log2**
</dt> <dd></dd> <dt>

**\_flag di \_ filtro ciclo PCM \_ disabilitato \_**
</dt> <dd></dd> <dt>

**\_ \_ \_ \_ flag present pics ref \_ a lungo termine** 
</dt> <dd></dd> <dt>

**\_flag di \_ \_ Abilitazione del MVP temporale SPS \_**
</dt> <dd></dd> <dt>

**\_flag Strong intra \_ smoothing \_ abilitato \_** 
</dt> <dd></dd> <dt>

**\_flag per segmenti di sezione dipendenti \_ \_ abilitato \_** 
</dt> <dd></dd> <dt>

**flag di output \_ flag \_ presente \_** 
</dt> <dd></dd> <dt>

**numero \_ di \_ \_ bit di intestazione di sezione aggiuntivi \_** 
</dt> <dd></dd> <dt>

**\_flag di \_ \_ Abilitazione Nascondi dati \_ firma**
</dt> <dd></dd> <dt>

**\_flag CABAC init \_ present \_**
</dt> <dd></dd> <dt>

**ReservedBits3** 
</dt> <dd></dd> <dt>

**dwCodingParamToolFlags**
</dt> <dd></dd> <dt>

**\_ \_ flag di indazione intra vincolato \_**
</dt> <dd></dd> <dt>

**\_flag di \_ Abilitazione della trasformazione ignora \_**
</dt> <dd></dd> <dt>

**\_flag di \_ \_ Abilitazione \_ Delta di cu QP**
</dt> <dd></dd> <dt>

**\_flag di \_ cromatura della sezione \_ \_ PPS \_ \_**
</dt> <dd></dd> <dt>

**\_flag prede ponderato \_**
</dt> <dd></dd> <dt>

**\_flag bipredator ponderato \_**
</dt> <dd></dd> <dt>

**\_ \_ flag di abilitazione bypass di transquant \_**
</dt> <dd></dd> <dt>

**\_flag abilitati riquadri \_** 
</dt> <dd></dd> <dt>

**\_flag di sincronizzazione del codice entropia \_ \_ abilitato \_** 
</dt> <dd></dd> <dt>

**\_flag di spaziatura uniforme \_** 
</dt> <dd></dd> <dt>

**\_flag ciclo \_ tra \_ riquadri \_ abilitati \_** 
</dt> <dd></dd> <dt>

**\_filtro ciclo \_ PPS \_ tra le \_ sezioni \_ abilitate \_ flag**
</dt> <dd></dd> <dt>

**flag di deblocking \_ \_ abilitato per l'override del filtro \_ \_**
</dt> <dd></dd> <dt>

**\_flag di deblocco del filtro di PPS \_ \_ disabilitato \_**
</dt> <dd></dd> <dt>

**\_ \_ flag presente elenco \_ modifiche**
</dt> <dd></dd> <dt>

**\_ \_ \_ \_ flag presente estensione intestazione segmento di sezione \_**
</dt> <dd></dd> <dt>

**IrapPicFlag**
</dt> <dd></dd> <dt>

**IdrPicFlag** 
</dt> <dd></dd> <dt>

**IntraPicFlag** 
</dt> <dd></dd> <dt>

**ReservedBits4** 
</dt> <dd></dd> <dt>

**dwCodingSettingPicturePropertyFlags**
</dt> <dd></dd> <dt>

**\_ \_ offset QP CB \_ PPS**
</dt> <dd></dd> <dt>

**\_offset CR \_ QP di PPS \_**
</dt> <dd></dd> <dt>

**num \_ \_ colonne riquadro \_ Minus1**
</dt> <dd></dd> <dt>

**numero \_ di \_ righe del riquadro \_ Minus1**
</dt> <dd></dd> <dt>

**\_Minus1 larghezza \_ colonna**
</dt> <dd></dd> <dt>

**\_altezza riga \_ Minus1**
</dt> <dd></dd> <dt>

**\_ \_ \_ profondità Delta QP diff \_ cu**
</dt> <dd></dd> <dt>

**\_offset beta di PPS \_ \_ div2**
</dt> <dd></dd> <dt>

**\_offset TC \_ PPS \_ div2**
</dt> <dd></dd> <dt>

**log2 \_ a \_ livello di merge parallelo \_ \_ Minus2**
</dt> <dd></dd> <dt>

**CurrPicOrderCntVal**
</dt> <dd></dd> <dt>

**RefPicList**
</dt> <dd></dd> <dt>

**ReservedBits5**
</dt> <dd></dd> <dt>

**PicOrderCntValList**
</dt> <dd></dd> <dt>

**RefPicSetStCurrBefore**
</dt> <dd></dd> <dt>

**RefPicSetStCurrAfter**
</dt> <dd></dd> <dt>

**RefPicSetLtCurr**
</dt> <dd></dd> <dt>

**ReservedBits6**
</dt> <dd></dd> <dt>

**ReservedBits7**
</dt> <dd></dd> <dt>

**StatusReportFeedbackNumber**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                      |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture di Media Foundation](media-foundation-structures.md)
</dt> </dl>

 

 




