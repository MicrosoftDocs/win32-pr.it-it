---
title: Proprietà VoiceCaption (oggetto Commands)
description: Informazioni sulla proprietà VoiceCaption dell'oggetto Commands, che restituisce o imposta il testo visualizzato per l'oggetto Commands nella finestra Comandi vocali.
ms.assetid: 2c4fa175-fc2d-4474-b15f-7e838103a435
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4a2113e0a952f253df901d192b42466fa30350
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396126"
---
# <a name="voicecaption-property-commands-object"></a>Proprietà VoiceCaption (oggetto Commands)

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta il testo visualizzato per [**l'oggetto Commands**](/windows/desktop/lwef/the-commands-collection-object) nella finestra Comandi vocali.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Stringa Commands.VoiceCaption_ *  \[  =  \]



| Parte     | Descrizione                                               |
|----------|-----------------------------------------------------------|
| *string* | Espressione stringa che restituisce il testo visualizzato. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Se si imposta la [**proprietà Voice**](voice-property.md) della raccolta [**Commands,**](/windows/desktop/lwef/the-commands-collection-object) in genere si imposta anche la **relativa proprietà VoiceCaption.** **L'impostazione di testo VoiceCaption** viene visualizzata nella finestra Comandi vocali quando l'applicazione client è attiva per l'input e il carattere è visibile. Se questa proprietà non è impostata, l'impostazione della proprietà [**Caption**](caption-property.md) della raccolta **Commands** determina il testo visualizzato. Quando nessuna delle due proprietà **VoiceCaption** o **Caption** è impostata, i comandi nella raccolta vengono visualizzati nella finestra Comandi vocali in "(comando non definito)" quando l'applicazione client diventa attiva per l'input.

**L'impostazione VoiceCaption** determina anche il testo visualizzato nel suggerimento di ascolto per indicare i comandi per cui il carattere è in ascolto.

## <a name="see-also"></a>Vedere anche

[Proprietà Caption](caption-property.md)


 

 
