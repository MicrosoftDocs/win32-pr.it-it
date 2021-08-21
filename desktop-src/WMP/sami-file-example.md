---
title: Esempio di file SAMI
description: Esempio di file SAMI
ms.assetid: 52b566f1-0d87-4bf2-87b3-3821e69a5699
keywords:
- Windows Media Player,Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player a oggetti, Synchronized Accessible Media Interchange (SAMI)
- modello a oggetti,Interscambio multimediale accessibile sincronizzato (SAMI)
- Windows Media Player Mobile,Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player ActiveX,Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player Controllo ActiveX mobile,Interscambio multimediale accessibile sincronizzato (SAMI)
- ActiveX,Synchronized Accessible Media Interchange (SAMI)
- Synchronized Accessible Media Interchange (SAMI), files
- SAMI (Synchronized Accessible Media Interchange),files
- Synchronized Accessible Media Interchange (SAMI), codice di esempio
- SAMI (Synchronized Accessible Media Interchange), codice di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d4e2ab5189f99118afae3fb2dae7374323cc8c16605bb458a04bd31810ed91a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569807"
---
# <a name="sami-file-example"></a>Esempio di file SAMI

Il codice di esempio seguente è un file SAMI completo con un set di testo di sottotitoli codificati e diverse dichiarazioni di classe per lo stile del testo e la lingua dei sottotitoli.


```C++
<SAMI>
<HEAD>
   <STYLE TYPE = "text/css">
   <!--
   /* P defines the basic style selector for closed caption paragraph text */
   P {font-family:sans-serif; color:white;}
   /* Source, Small, and Big define additional ID selectors for closed caption text */
   #Source {color: orange; font-family: arial; font-size: 12pt;}
   #Small {Name: SmallTxt; font-size: 8pt; color: yellow;}
   #Big {Name: BigTxt; font-size: 12pt; color: magenta;}
   /* ENUSCC and FRFRCC define language class selectors for closed caption text */
   .ENUSCC {Name: 'English Captions'; lang: en-US; SAMIType: CC;}
   .FRFRCC {Name: 'French Captions'; lang: fr-FR; SAMIType: CC;}
   -->
   </STYLE>
</HEAD>
<BODY>
   <!<entity type="mdash"/>- The closed caption text displays at 1000 milliseconds. -->
   <SYNC Start = 1000>
      <!-- English closed captions -->
      <P Class = ENUSCC ID = Source>Narrator
      <P Class = ENUSCC>Great reason to visit Seattle, brought to you by two out-of-staters.
      <!-- French closed captions -->
      <P Class = FRFRCC ID = Source>Narrateur
      <P Class = FRFRCC>Deux personnes ne venant la r&eacute;gion vous donnent de bonnes raisons de visiter Seattle.
</BODY>
</SAMI>

```



Gli stili definiti all'interno di un file SAMI sono conformi alla sintassi del selettore CSS standard per elementi, classi e ID. Nell'elemento BODY tutti gli elementi P hanno lo stile definito per il selettore di elementi P nell'elemento STYLE. L'attributo class di un elemento specifica il linguaggio di tale elemento come definito dai selettori di classe nell'elemento STYLE (i selettori che iniziano con punti). I nomi delle lingue specificati dai selettori di classe possono essere qualsiasi stringa. Agli elementi con l'attributo ID specificato viene applicato uno stile aggiuntivo, come indicato dai selettori ID nell'elemento STYLE (i selettori preceduti da \# caratteri).

Se usati in combinazione con il Windows Media Player a oggetti, i selettori di classe corrispondono a *ClosedCaption*. **Proprietà SAMILang,** che può essere usata per specificare la lingua dei sottotitoli. I selettori ID corrispondono a *ClosedCaption.* **Proprietà SAMIStyle,** che può essere usata per specificare lo stile in cui verranno visualizzati i sottotitoli.

Per altre informazioni sulla creazione di file SAMI, vedere Informazioni su SAMI 1.0 nel sito [Web Microsoft.](/documentation/)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Aggiunta di sottotitoli codificati ai supporti digitali**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 