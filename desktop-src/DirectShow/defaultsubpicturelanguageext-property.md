---
description: Tramite la proprietà DefaultSubpictureLanguageExt viene recuperata l'estensione predefinita per il linguaggio dell'immagine di DVD.
ms.assetid: bd437844-6e5c-4237-a968-700a53e18635
title: Proprietà DefaultSubpictureLanguageExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37bba455a26df4eaa6676b77447c3faed408609
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520746"
---
# <a name="defaultsubpicturelanguageext-property"></a>Proprietà DefaultSubpictureLanguageExt

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Tramite la `DefaultSubpictureLanguageExt` proprietà viene recuperata l'estensione predefinita per il linguaggio della sottoimmagine DVD.

``` syntax
[ iLangExt = ] MSWebDVD.DefaultSubpictureLanguageExt
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che indica l'estensione predefinita per il linguaggio di sottoimmagine DVD.

## <a name="remarks"></a>Commenti

Questa proprietà è di sola lettura e non prevede alcun valore predefinito. Nella tabella seguente sono illustrati i possibili valori.



| Valore | Descrizione                    |
|-------|--------------------------------|
| 0     | Estensione non specificata        |
| 1     | Didascalie normali                |
| 2     | Didascalie grandi                   |
| 3     | Didascalie degli elementi figlio            |
| 5     | Didascalie normali chiuse         |
| 6     | Didascalie grandi chiuse            |
| 7     | Didascalie chiuse degli elementi figlio     |
| 9     | Forced                         |
| 13    | Commenti del normale Director     |
| 14    | Commenti di Big Director        |
| 15    | Commenti del direttore per gli elementi figlio |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SelectDefaultSubpictureLanguage**](selectdefaultsubpicturelanguage-method.md)
</dt> </dl>

 

 



