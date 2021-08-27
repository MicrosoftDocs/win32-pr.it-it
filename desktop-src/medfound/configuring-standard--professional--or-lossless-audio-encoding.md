---
description: Quando il Windows media audio enumera i tipi di output, identifica ogni tipo enumerato come Standard, Professional o Senza perdita di dati.
ms.assetid: 1c3d22c3-10f7-454a-b1c1-372d684b6568
title: Configurazione della codifica audio standard, Professional o senza perdita di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fa4184af8bc6b83710a3710ac1a278de71de0b7221dc11757bdeba46af8c7c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743538"
---
# <a name="configuring-standard-professional-or-lossless-audio-encoding"></a>Configurazione della codifica audio standard, Professional o senza perdita di dati

Quando il Windows media audio enumera i tipi di output, identifica ogni tipo enumerato come Standard, Professional o Senza perdita di dati. È possibile determinare se un tipo di output è Standard, Professional o Lossless seguendo questa procedura.

1.  Chiamare [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) per ottenere [**un'interfaccia IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) che rappresenta il tipo di output.
2.  Chiamare [**IMFMediaType::GetRepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation) per ottenere una struttura [**AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) contenente informazioni sul tipo di output.
3.  Il **membro pbFormat** della struttura [**AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) punta a una [**struttura WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) che contiene informazioni aggiuntive sul tipo di output. Esaminare il **membro wFormatTag** della **struttura WAVEFORMATEX.** Un valore 0x161 indica Standard, un valore 0x162 indica Professional e un valore 0x163 indica Senza perdita di dati.

Se si impostano le proprietà nel Windows Media Audio encoder prima di enumerare i tipi di output, è possibile limitare il numero di tipi di output enumerati. Ad esempio, se si impostano le proprietà VBR in modo appropriato, è possibile limitare i tipi di output enumerati a quelli della categoria Senza perdita di dati.

## <a name="standard-audio-encoding"></a>Codifica audio standard

È possibile usare la procedura seguente per configurare la codifica audio standard.

1.  Impostare le proprietà di propria scelta nel codificatore.
2.  Enumerare i tipi di output possibili.
3.  Esaminare i tipi enumerati e sceglierne uno con un tag di formato audio 0x161.
4.  Impostare il tipo di output sul tipo scelto chiamando [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

## <a name="professional-audio-encoding"></a>Professional Codifica audio

È possibile usare la procedura seguente per configurare Professional codifica audio.

1.  Impostare le proprietà di propria scelta nel codificatore.
2.  Enumerare i tipi di output possibili.
3.  Esaminare i tipi enumerati e sceglierne uno con un tag di formato audio 0x162.
4.  Impostare il tipo di output sul tipo scelto chiamando [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

## <a name="lossless-audio-encoding"></a>Codifica audio senza perdita di dati

È possibile usare la procedura seguente per configurare la codifica audio senza perdita di dati.

1.  Impostare la [**proprietà MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) su **VARIANT \_ TRUE.**
2.  Impostare la [**proprietà MFPKEY \_ CONSTRAIN \_ ENUMERATED \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) su **VARIANT \_ TRUE.**
3.  Impostare la [**proprietà MFPKEY \_ DESIRED \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) su 100.
4.  Enumerare i tipi di output.
5.  Impostare il tipo di output su uno dei tipi enumerati nel passaggio 4 chiamando [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

Il codice seguente enumera tutti i tipi di output senza perdita di dati per il Windows Media Audio. Il codice stampa il valore del tag di formato audio per ogni tipo enumerato. Poiché tutti i tipi enumerati sono senza perdita di dati, tutti questi tag di formato hanno un valore di 0x163. Si supponga che pIMT sia un puntatore a un'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in un oggetto codificatore di Windows Media Audio e che pStore sia un puntatore a **un'interfaccia IPropertyStore** sullo stesso oggetto. Si supponga anche che hr sia una variabile di **tipo HRESULT** dichiarata in precedenza nel codice.


```
PROPVARIANT prop;
prop.vt = VT_BOOL;
prop.boolVal = VARIANT_TRUE;
hr = pStore->SetValue(MFPKEY_VBRENABLED, prop);

if(SUCCEEDED(hr))
{
   hr = pStore->SetValue(MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY, prop);

   if(SUCCEEDED(hr))
   {
      prop.vt = VT_UI4;
      prop.ulVal = 100;
      hr = pStore->SetValue(MFPKEY_DESIRED_VBRQUALITY, prop);
      
      if(SUCCEEDED(hr))
      {           
         HRESULT hrAvailableType = S_OK;
         LONG j = 0;
         while(MF_E_NO_MORE_TYPES != hrAvailableType)
         {
            IMFMediaType* pOutputType = NULL;     
            hrAvailableType = pIMFT->GetOutputAvailableType(
               0, j, &pOutputType);

            if(SUCCEEDED(hrAvailableType))
            {
               AM_MEDIA_TYPE* pTypeRep = NULL;
               hr = pOutputType->GetRepresentation(
                  AM_MEDIA_TYPE_REPRESENTATION, (VOID**)&pTypeRep); 
                     
               if(SUCCEEDED(hr))
               {
                  WAVEFORMATEX* pwfex = (WAVEFORMATEX*)pTypeRep->pbFormat;
                  printf_s("%x\n", pwfex->wFormatTag);
                  pOutputType->FreeRepresentation(
                     AM_MEDIA_TYPE_REPRESENTATION, (VOID*)pTypeRep);
               }

               pOutputType->Release();
               ++j;
            }                                                                  
         } // while                 
      }                                
   } 
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione della codifica audio](configuringaudioencoding.md)
</dt> </dl>

 

 
