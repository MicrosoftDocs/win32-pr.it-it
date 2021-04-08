---
description: Quando il codificatore Windows Media Audio enumera i tipi di output, identifica ogni tipo enumerato come standard, Professional o lossless.
ms.assetid: 1c3d22c3-10f7-454a-b1c1-372d684b6568
title: Configurazione della codifica audio standard, Professional o lossless
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e781c2c093b46a12fa4ad5434f97931a948ff9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749335"
---
# <a name="configuring-standard-professional-or-lossless-audio-encoding"></a>Configurazione della codifica audio standard, Professional o lossless

Quando il codificatore Windows Media Audio enumera i tipi di output, identifica ogni tipo enumerato come standard, Professional o lossless. È possibile determinare se un tipo di output è standard, Professional o lossless attenendosi alla procedura seguente.

1.  Chiamare [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) per ottenere un'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) che rappresenta il tipo di output.
2.  Chiamare [**IMFMediaType:: Getrappresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation) per ottenere una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) che contiene informazioni sul tipo di output.
3.  Il membro **pbFormat** della struttura [**del \_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) punta a una struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) che contiene informazioni aggiuntive sul tipo di output. Esaminare il membro **wFormatTag** della struttura **WAVEFORMATEX** . Il valore 0x161 indica standard, il valore 0x162 indica Professional e il valore 0x163 indica senza perdita di valori.

Se si impostano le proprietà nel codificatore Windows Media Audio prima di enumerare i tipi di output, è possibile limitare il numero di tipi di output enumerati. Se ad esempio si impostano le proprietà VBR in modo appropriato, è possibile limitare i tipi di output enumerati a quelli presenti nella categoria lossless.

## <a name="standard-audio-encoding"></a>Codifica audio standard

Per configurare la codifica audio standard, è possibile usare i passaggi seguenti.

1.  Impostare le proprietà scelte nel codificatore.
2.  Enumerare i tipi di output possibili.
3.  Esaminare i tipi enumerati e sceglierne uno con un tag di formato audio 0x161.
4.  Impostare il tipo di output sul tipo scelto chiamando [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

## <a name="professional-audio-encoding"></a>Codifica audio professionale

Per configurare la codifica audio professionale, è possibile usare i passaggi seguenti.

1.  Impostare le proprietà scelte nel codificatore.
2.  Enumerare i tipi di output possibili.
3.  Esaminare i tipi enumerati e sceglierne uno con un tag di formato audio 0x162.
4.  Impostare il tipo di output sul tipo scelto chiamando [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

## <a name="lossless-audio-encoding"></a>Codifica audio senza perdita di contenuti

Per configurare la codifica audio senza perdita di codice, è possibile usare i passaggi seguenti.

1.  Impostare la proprietà [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) su **Variant \_ true**.
2.  Impostare la proprietà [**MFPKEY \_ vincolate \_ Enumerated \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) su **Variant \_ true**.
3.  Impostare la proprietà [**MFPKEY \_ desired \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) su 100.
4.  Enumerare i tipi di output.
5.  Impostare il tipo di output su uno dei tipi enumerati nel passaggio 4 chiamando [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

Il codice seguente enumera tutti i tipi di output lossless per il codificatore Windows Media Audio. Il codice stampa il valore del tag di formato audio per ogni tipo enumerato. Poiché tutti i tipi enumerati sono lossless, tutti i tag di formato hanno un valore 0x163. Si supponga che pIMT sia un puntatore a un'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) su un oggetto Windows Media Audio Encoder e che pStore sia un puntatore a un'interfaccia **IPropertyStore** sullo stesso oggetto. Si supponga inoltre che HR sia una variabile di tipo **HRESULT** dichiarata in precedenza nel codice.


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

 

 
