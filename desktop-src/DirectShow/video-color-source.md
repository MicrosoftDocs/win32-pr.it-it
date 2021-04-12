---
description: Origine colore video
ms.assetid: e6addd55-06ca-4d4b-b2b0-fde281fab244
title: Origine colore video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e9c751d74a78b027d50f033acb3709d18fe8f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232281"
---
# <a name="video-color-source"></a>Origine colore video

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L'origine colori video crea un'immagine video continua di un colore a tinta unita.

ID classe (CLSID): **{0CFDD070-581A-11D2-9EE6-006008039E37}**

Nome variabile CLSID: **CLSID \_ ColorSource**

Proprietà



| Proprietà | Type      | Predefinito | Descrizione                                   |
|----------|-----------|---------|-----------------------------------------------|
| Colore  | **DWORD** | 0       | Specifica il colore da generare. Vedere la sezione Osservazioni. |



 

## <a name="remarks"></a>Commenti

L'origine dei colori video viene utilizzata con gli oggetti di origine. Per prima cosa, creare un nuovo oggetto di origine. Impostare quindi il GUID dell'oggetto di origine su CLSID \_ ColorSource, chiamando il metodo [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) .

Per impostare il colore, creare un oggetto [setter della proprietà](property-setter.md) e applicare la proprietà "color" all'ora zero. Il valore di questa proprietà è un numero esadecimale con formato *0xAARRGGBB*, dove *AA* è il valore alfa, *RR* è il valore rosso, *GG* è il valore verde e *BB* è il valore blu. I valori alfa variano da 0x00 (trasparente) a 0xFF (opaco). La proprietà è statica e deve essere applicata all'ora zero.

Se non si specifica il valore alfa, il valore predefinito è zero (trasparente). In un progetto video a colori a 32 bit, questa operazione causerà transizioni o effetti che usano Alpha per eseguire il rendering dell'origine del colore del video come completamente trasparente. Per essere sicuri, specificare sempre l'alfa. Ad esempio, il nero opaco è **0xFF000000**.

Nell'esempio di codice riportato di seguito viene illustrato come utilizzare questo oggetto. Per ulteriori informazioni sull'utilizzo di [**IPropertySetter**](ipropertysetter.md), vedere [impostazione delle proprietà relative a effetti e transizioni](setting-properties-on-effects-and-transitions.md):


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



Nell'esempio seguente viene illustrata la rappresentazione XML dell'oggetto creato nell'esempio precedente. In questo caso l'elemento [**param**](param-element.md) non supporta gli elementi [**in**](at-element.md) o [**lineari**](linear-element.md) , perché l'oggetto non supporta le proprietà dinamiche:


```C++
<clip start="0" stop="5" clsid="{0CFDD070-581A-11D2-9EE6-006008039E37}">
    <param name="Color" value="16776960"/>
</clip>
```



 

 



