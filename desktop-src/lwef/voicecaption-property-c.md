---
title: Proprietà VoiceCaption (oggetto Command)
description: Proprietà VoiceCaption
ms.assetid: 97a3015c-6c39-42d5-b6bd-7563bd444b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1077c8d65a52bc8f0cfa329fdceb740e30e6784
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300819"
---
# <a name="voicecaption-property-command-object"></a>Proprietà VoiceCaption (oggetto Command)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Imposta o restituisce il testo visualizzato per l'oggetto [**Command**](/windows/desktop/lwef/the-command-object) nella finestra dei comandi vocali.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*Agent. ***Characters ("**_CharacterID_*_"). Comandi ("_*_Name_*_")._ *  \[  =  *Stringa* VoiceCaption\]



| Parte     | Descrizione                                               |
|----------|-----------------------------------------------------------|
| *string* | Espressione stringa che restituisce il testo visualizzato. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Se si definisce un oggetto [**Command**](/windows/desktop/lwef/the-command-object) in una raccolta di [**comandi**](https://www.bing.com/search?q=**Commands**) e si imposta la relativa proprietà [**Voice**](voice-property.md) , in genere viene impostata anche la relativa proprietà [**VoiceCaption**](voicecaption-property.md) . Questo testo verrà visualizzato nella finestra comandi vocali quando l'applicazione client è di input-attivo e il carattere è visibile. Se questa proprietà non è impostata, l'impostazione per la proprietà [**Caption**](caption-property.md) determina il testo visualizzato. Quando non viene impostata la proprietà **VoiceCaption** né **Caption** , il comando non viene visualizzato nella finestra dei comandi vocali.

### <a name="see-also"></a>Vedere anche

[**Proprietà Caption**](caption-property.md)


 

 
