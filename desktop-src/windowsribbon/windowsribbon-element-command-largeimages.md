---
title: Proprietà Command.LargeImages
description: Rappresenta un contenitore di immagini. in questo caso, immagini di grandi dimensioni.
ms.assetid: 9fcd3694-7847-43e2-9877-47daf47aae9a
keywords:
- Proprietà Command.LargeImages Windows ribbon
topic_type:
- apiref
api_name:
- Command.LargeImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66214eb05910296b2c03a749d88134bef68f86badc2ffd7f7b69d0ba6adfdd5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931617"
---
# <a name="commandlargeimages-property"></a>Proprietà Command.LargeImages

Rappresenta un contenitore di immagini. in questo caso, immagini di grandi dimensioni.

## <a name="usage"></a>Utilizzo

``` syntax
<Command.LargeImages>
  child elements
</Command.LargeImages>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                 | Descrizione                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [**Immagine**](windowsribbon-element-image.md)<br/> | Può verificarsi una o più volte<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                     |
|-------------------------------------------------------------|
| [**Comando**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi al massimo una volta per ogni [**comando**](windowsribbon-element-command.md).

Le risorse immagine devono essere conformi al formato grafico BMP (Standard Bitmap) usato Windows.

## <a name="examples"></a>Esempio

L'esempio seguente illustra il markup di base per [**SplitButton**](windowsribbon-element-splitbutton.md) con un [**elemento MenuGroup.**](windowsribbon-element-menugroup.md)

Questa sezione di codice illustra le [**dichiarazioni di comando SplitButton**](windowsribbon-element-splitbutton.md) e [**MenuGroup**](windowsribbon-element-menugroup.md) con una risorsa immagine di grandi dimensioni e una piccola. Viene dichiarato [**anche un**](windowsribbon-element-group.md) gruppo associato che funge da contenitore padre per **l'elemento SplitButton.**


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Specifica delle risorse immagine della barra multifunzione](windowsribbon-imageformats.md)
</dt> <dt>

[UI \_ PKEY \_ LargeImage](windowsribbon-reference-properties-uipkey-largeimage.md)
</dt> </dl>

 

 





