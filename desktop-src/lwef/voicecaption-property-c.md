---
title: Proprietà VoiceCaption (oggetto Command)
description: Informazioni sulla proprietà VoiceCaption dell'oggetto Command, che imposta o restituisce il testo visualizzato per l'oggetto Command nella finestra Comandi vocali.
ms.assetid: 97a3015c-6c39-42d5-b6bd-7563bd444b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d700b5d29b4c493be7382d45de55f44e6d02646c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396166"
---
# <a name="voicecaption-property-command-object"></a>Proprietà VoiceCaption (oggetto Command)

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Imposta o restituisce il testo visualizzato per [**l'oggetto Command**](/windows/desktop/lwef/the-command-object) nella finestra Comandi vocali.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Commands("_*_Name_*_"). Stringa_ *  \[  =  *VoiceCaption*\]



| Parte     | Descrizione                                               |
|----------|-----------------------------------------------------------|
| *string* | Espressione stringa che restituisce il testo visualizzato. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Se si definisce un [**oggetto Command**](/windows/desktop/lwef/the-command-object) in una raccolta [**Commands**](https://www.bing.com/search?q=**Commands**) e si imposta la relativa [**proprietà Voice,**](voice-property.md) in genere si imposta anche la [**relativa proprietà VoiceCaption.**](voicecaption-property.md) Questo testo verrà visualizzato nella finestra Comandi vocali quando l'applicazione client è attiva per l'input e il carattere è visibile. Se questa proprietà non è impostata, l'impostazione della [**proprietà Caption**](caption-property.md) determina il testo visualizzato. Quando la proprietà **VoiceCaption** e **Caption** non è impostata, il comando non viene visualizzato nella finestra Comandi vocali.

### <a name="see-also"></a>Vedere anche

[**Caption - proprietà**](caption-property.md)


 

 
