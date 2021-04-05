---
description: Fusione alfa
ms.assetid: 56618e74-32cc-48f8-83b6-4fc31ab6fc36
title: Fusione alfa (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4293448849926cfc6723495619137262e004636e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125208"
---
# <a name="alpha-blending-directshow"></a>Fusione alfa (DirectShow)

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Questo articolo descrive la fusione alfa in [DirectShow editing Services](directshow-editing-services.md) (des).

Alfa misura la trasparenza di un pixel o di un'immagine. Nel video RGB non compresso a 32 bit, quattro componenti definiscono ogni pixel, ovvero un canale alfa (A) e tre componenti colore (RGB). Un pixel con un valore alfa pari a zero è completamente trasparente. Un pixel con un valore alfa pari a 255 è opaco. Tra questi valori, il pixel presenta diversi gradi di trasparenza.

DirectShow definisce due tipi di supporto per video RGB a 32 bit:

-   **MEDIASUBTYPE \_ ARGB32**: il video è di 32 bit RGB con un canale alfa valido.
-   **MEDIASUBTYPE \_ RGB32**: i pixel sono 32 bit, ma il canale alfa non è necessariamente valido.

Per eseguire la fusione alfa in DES, impostare il tipo di supporto non compresso del gruppo video su MEDIASUBTYPE \_ ARGB32. In C++ chiamare il metodo [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md) . Nel formato XTL impostare anche l'attributo [**bitdepth**](bitdepth-attribute.md) dell'elemento [**Group**](group-element.md) su 32.

Sono quindi necessari dati video contenenti un canale alfa. Sono disponibili diverse opzioni:

-   È possibile usare un file AVI che ha già un video RGB a 32 bit con dati Alpha. Attualmente, Alpha non è supportato per i file di origine MPEG o Microsoft Windows Media Format (WMF).
-   DES supporta i file di bitmap a 32 bit (BMP) e targa (. tga) con dati alfa.
-   È possibile scrivere un filtro di origine personalizzato che crea dati RGB a 32 bit con Alpha. Il tipo di supporto di output deve essere **MEDIASUBTYPE \_ ARGB32**. Usare il filtro come sottooggetto in un oggetto di origine della sequenza temporale.

Se l'origine video non dispone di alfa, è possibile usare un effetto che consente di creare dati alfa. L' [effetto Alpha Setter](alpha-setter-effect.md) imposta il canale alfa per l'intera immagine su un valore costante. Per variare l'alfa nel tempo, usare l'interfaccia [**IPropertySetter**](ipropertysetter.md) con l'effetto di Setter alfa. Non è necessario che l'origine originale sia 32 bit, purché il tipo di supporto non compresso del gruppo sia **MEDIASUBTYPE \_ ARGB32**.

Infine, passare il video a un effetto o una transizione che esegue la fusione alfa. La [transizione del Compositor](compositor-transition.md) esegue la fusione alfa e la [transizione della chiave](key-transition.md) può essere chiave in base al valore alfa.

Il progetto XTL di esempio seguente esegue la fusione alfa:


```C++
<timeline>
<group type="video" bitdepth="32" width="320" height="240">
<track>
  <clip start="0" stop="6" src="c:\Example.avi" />
</track>
<track>
  <clip start="0" stop="6" src="c:\Example2.avi">
    <!-- Alpha Setter effect. -->
    <effect clsid="{506D89AE-909A-44f7-9444-ABD575896E35}" start="0" stop="6">
      <param name="alpha" value="255">
        <linear time="6" value="0" />
      </param>
    </effect>
  </clip>
  <!-- Key transition, with alpha keying. -->
  <transition clsid="{C5B19592-145E-11d3-9F04-006008039E37}" start="0" stop="6">
    <param name="KeyType" value="3" />  
  </transition>
</track>
</group>
</timeline>
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei servizi di modifica DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 



