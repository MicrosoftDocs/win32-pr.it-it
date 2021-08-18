---
description: Origine colore video
ms.assetid: e6addd55-06ca-4d4b-b2b0-fde281fab244
title: Origine colore video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 331640a9240ef0ea16ff565180503066f22ce5ae2550fa1e1ec524dcf05c8fa5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071935"
---
# <a name="video-color-source"></a>Origine colore video

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

L'origine colore video crea un'immagine video continua di un colore a tinta unita.

ID classe (CLSID): **{0CFDD070-581A-11D2-9EE6-006008039E37}**

Nome variabile CLSID: **CLSID \_ ColorSource**

Proprietà



| Proprietà | Type      | Predefinito | Descrizione                                   |
|----------|-----------|---------|-----------------------------------------------|
| "Color"  | **Dword** | 0       | Specifica il colore da generare. Vedere la sezione Osservazioni. |



 

## <a name="remarks"></a>Commenti

L'origine colore video viene usata con gli oggetti di origine. Creare prima di tutto un nuovo oggetto di origine. Impostare quindi il GUID dell'oggetto secondario dell'oggetto di origine su CLSID \_ ColorSource, chiamando il [**metodo IAMTimelineObj::SetSubObjectGUID.**](iamtimelineobj-setsubobjectguid.md)

Per impostare il colore, creare un [oggetto Property Setter](property-setter.md) e applicare la proprietà "Color" all'ora zero. Il valore di questa proprietà è un numero esadecimale nel formato *0xAARRGGBB*, dove *AA* è il valore alfa, *RR* è il valore rosso, *GG* è il valore verde e *BB* è il valore blu. I valori alfa sono 0x00 (trasparente) a 0xFF (opaco). La proprietà è statica e deve essere applicata al momento zero.

Se non si specifica il valore alfa, il valore predefinito è zero (trasparente). In un progetto video a 32 bit, ciò causerà transizioni o effetti che usano alfa per eseguire il rendering dell'origine colore video come completamente trasparente. Per sicurezza, specificare sempre il valore alfa. Ad esempio, il nero opaco **è 0xFF000000**.

Nell'esempio di codice seguente viene illustrato come utilizzare questo oggetto . Per altre informazioni [**sull'uso di IPropertySetter,**](ipropertysetter.md)vedere [Impostazione delle proprietà su effetti e transizioni:](setting-properties-on-effects-and-transitions.md)


```C++
DWORD           dwYellow = 0xFFFF00;
IAMTimelineObj  *pSource = NULL;

// Create the source.
HRESULT hr = pTimeline->CreateEmptyNode(&pSource, TIMELINE_MAJOR_TYPE_SOURCE);
if (SUCCEEDED(hr))
{
    hr = pSource->SetStartStop(0, 50000000);
}

if (SUCCEEDED(hr))
{
    hr = pSource->SetSubObjectGUID(CLSID_ColorSource);
}

// Create a property setter.
if (SUCCEEDED(hr))
{
    IPropertySetter *pProp = NULL;
    
    hr = CoCreateInstance(CLSID_PropertySetter, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pProp));

    if SUCCEEDED(hr))
    {
        // Set the color.    
        DEXTER_PARAM param;
        DEXTER_VALUE val;

        param.Name = SysAllocString(OLESTR("Color"));
        param.dispID = 0;
        param.nValues = 1;

        if (param.Name == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            val.v.vt = VT_I4;
            val.v.lVal = dwYellow;
            val.rt = 0;  // Time must be zero.
            val.dwInterp = DEXTERF_JUMP;

            hr = pProp->AddProp(param, &val);
            
            SysFreeString(param.Name);
        }

        if (SUCCEEDED(hr))
        {
            hr = pSource->SetPropertySetter(pProp); 
        }
        pProp->Release();
    }
}
```



Nell'esempio seguente viene illustrata la rappresentazione XML dell'oggetto creato nell'esempio precedente. In questo caso [**l'elemento param**](param-element.md) non supporta [**gli elementi in corrispondenza di**](at-element.md) o [**lineari,**](linear-element.md) perché l'oggetto non supporta le proprietà dinamiche:


```C++
<clip start="0" stop="5" clsid="{0CFDD070-581A-11D2-9EE6-006008039E37}">
    <param name="Color" value="16776960"/>
</clip>
```



 

 



