---
description: I GUID seguenti supportano le API video Direct3D 12.
ms.assetid: CF2F3058-328A-4128-B5C6-29723B49AB1E
title: GUID video Direct3D 12 (d3d11. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05f7a56227ccc2953504d8466a34d6b2160ce1e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225810"
---
# <a name="direct3d-12-video-guids"></a>GUID video Direct3D 12

I GUID seguenti supportano le API video Direct3D 12.

## <a name="d3d12_video_decode_profile-guids"></a>D3D12 \\ _VIDEO \\ _DECODE \\ GUID _PROFILE

La tabella seguente elenca i GUID che identificano i profili di decodifica video Direct3D 12. Le descrizioni riguardano ogni profilo di decodifica video Direct3D 12 per il profilo Direct3D 11 o DXVA equivalente.

| Nome                                                 | Valore                                                                                | Descrizione
|------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| D3D12 \_ video \_ Decode \_ profile \_ MPEG1 \_ e \_ MPEG2           | 0x86695f12, 0x340e, 0x4f04, 0x9F, 0xD3, 0x92, 0x53, 0xDD, 0x32, 0x74, 0x60 | Equivale a DXVA2 \_ ModeMPEG2and1 \_ VLD.                 |
| D3D12 \_ video \_ Decode \_ profile \_ MPEG2                     | 0xee27417f, 0x5e28, 0x4e65, 0xBE, 0xEA, 0x1d, 0x26, 0xB5, 0x08, 0xAD, 0xC9           | Equivale a D3D11 \_ decoder \_ profile \_ MPEG2 \_ VLD e DXVA2 \_ ModeMPEG2 \_ VLD.                 |
| D3D12 \_ video \_ Decode \_ profile \_ H264                      | 0x1b81be68, 0xa0c7, 0x11d3, 0xb9, 0x84, 0x00, 0xC0, 0x4F, 0x2E, 0x73, 0xC5       | Equivale a D3D11 \_ decoder \_ profile \_ H264 \_ VLD \_ NOFGT e DXVA \_ ModeH264 \_ \_ VLD NOFGT. |
| D3D12 \_ video \_ Decode \_ profile \_ H264 \_ stereo \_ progressive   | 0xd79be8da, 0x0cf1, 0x4c81, 0xB8, 0x2A, 0x69, 0xA4, 0xe2, 0x36, 0xF4, 0x3D          | Equivale a D3D11 \_ decoder \_ profile \_ H264 \_ VLD \_ stereo \_ progressive \_ NOFGT e DXVA \_ ModeH264 \_ VLD \_ stereo \_ progressive \_ NOFGT. |
| D3D12 \_ video \_ Decode \_ profile \_ H264 \_ stereo               | 0xf9aaccbb, 0xc2b6, 0x4cfc, 0x87, 0x79, 0x57, 0x07, 0xB1, 0x76, 0x05, 0x52          | Equivalente a D3D11 \_ decoder \_ profile \_ H264 \_ VLD \_ stereo \_ NOFGT e DXVA \_ ModeH264 \_ VLD \_ stereo \_ NOFGT |
| D3D12 \_ video \_ Decode \_ profile \_ H264 \_ MultiView            | 0x705b9d82, 0x76cf, 0x49d6, 0xB7, 0xE6, 0xAC, 0x88, 0x72, 0xDB, 0x01, 0x3C          | Equivale a D3D11 \_ decoder \_ profile \_ H264 \_ VLD \_ MultiView \_ NOFGT e DXVA \_ ModeH264 \_ VLD \_ MultiView \_ NOFGT. |
| D3D12 \_ \_ profilo decodifica video \_ \_ VC1                       | 0x1b81beA3, 0xa0c7, 0x11d3, 0xb9, 0x84, 0x00, 0xC0, 0x4F, 0x2E, 0x73, 0xC5          | Equivale a D3D11 \_ decoder \_ profile \_ VC1 \_ VLD e DXVA \_ ModeVC1 \_ VLD. |
| D3D12 \_ \_ \_ \_ VC1 \_ D2010                 | 0x1b81beA4, 0xa0c7, 0x11d3, 0xb9, 0x84, 0x00, 0xC0, 0x4F, 0x2E, 0x73, 0xC5          | Equivale a D3D11 \_ decoder \_ profile \_ VC1 \_ D2010 e DXVA \_ ModeVC1 \_ D2010. |
| D3D12 \_ \_ profilo decodifica video \_ \_ MPEG4PT2 \_ Simple           | 0xefd64d74, 0xc9e8, 0x41d7, 0xA5, 0xE9, 0xE9, 0XB0, 0xE3, 0x9F, 0xA3, 0x19          | Equivale a D3D11 \_ decoder \_ profile \_ MPEG4PT2 \_ VLD \_ Simple e DXVA \_ ModeMPEG4pt2 \_ VLD \_ Simple. |
| D3D12 \_ video \_ Decode \_ profile \_ MPEG4PT2 \_ ADVSIMPLE \_ NOGMC  | 0xed418a9f, 0x010d, 0x4eda, 0x9A, 0xE3, 0x9A, 0x65, 0x35, 0x8d, 0x8d, 0x2E          | Equivale a D3D11 \_ decoder \_ profile \_ MPEG4PT2 \_ VLD \_ ADVSIMPLE \_ NOGMC e \_ \_ \_ \_ DXVA ModeMPEG4pt2 VLD ADVSIMPLE NOGMC. |
| D3D12 \_ video \_ Decode \_ profile \_ HEVC \_ Main                 | 0x5b11d51b, 0x2f4c, 0x4452, 0xBC, 0xC3, 0x09, 0xF2, 0xa1, 0x16, 0x0C, 0xC0          | Equivalente a D3D11 \_ decoder \_ profile \_ HEVC \_ VLD \_ Main e DXVA \_ ModeHEVC \_ VLD \_ Main
| D3D12 \_ \_ \_ \_ HEVC \_ MAIN10               | 0x107af0e0, 0xef1a, 0x4d19, 0xab, 0xA8, 0x67, 0xa1, 0x63, 0x07, 0x3D, 0x13          | Equivale a D3D11 \_ decoder \_ profile \_ HEVC \_ VLD \_ MAIN10 e DXVA \_ \_ \_ ModeHEVC VLD MAIN10.
| D3D12 \_ \_ profilo decodifica video \_ \_ VP9                       | 0x463707f8, 0xa1d0, 0x4585, 0x87, 0x6D, 0x83, 0xAA, 0x6D, 0x60, 0xB8, 0x9e | |
| D3D12 \_ video \_ Decode \_ profile \_ VP9 \_ 10 bit \_ profile2        | 0xa4c749ef, 0x6ecf, 0x48aa, 0x84, 0x48, 0x50, 0xA7, 0xa1, 0x16, 0x5F, 0xF7           | |
| D3D12 \_ \_ profilo decodifica video \_ \_ VP8                       | 0x90b899ea, 0x3a62, 0x4705, 0x88, 0xB3, 0x8d, 0xF0, 0x4b, 0x27, 0x44, 0xE7 | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_PROFILE0                       | 0xb8be4ccb, 0xcf53, 0x46ba, 0x8d, 0x59, 0xD6, 0xB8, 0xA6, 0xda, 0x5D, 0x2A | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_PROFILE1                       | 0x6936ff0f, 0x45b1, 0x4163, 0x9C, 0xC1, 0x64, 0x6E, 0XF6, 0x94, 0x61, 0x08 | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_PROFILE2                       | 0x0c5f2aa1, 0xe541, 0x4089, 0xBB, 0x7B, 0x98, 0x11, 0x0A, 0x19, 0xD7, 0xC8 | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_12BIT_PROFILE2                 | 0x17127009, 0xa00f, 0x4ce1, 0x99, 0x4E, 0xBF, 0x40, 0x81, 0XF6, 0xf3, 0xF0 | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_12BIT_PROFILE2_420             | 0x2d80bed6, 0x9cac, 0x4835, 0x9E, 0x91, 0x32, 0x7B, 0xBC, 0x4F, 0x9E, 0xE8 | |

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>D3d11. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[API video Direct3D 11](direct3d-11-video-apis.md)
</dt> </dl>

 

 




