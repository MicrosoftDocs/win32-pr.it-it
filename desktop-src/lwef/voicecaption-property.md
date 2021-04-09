---
title: Proprietà VoiceCaption (oggetto Commands)
description: Proprietà VoiceCaption
ms.assetid: 2c4fa175-fc2d-4474-b15f-7e838103a435
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa7d4a8ea9ff1cdd4a5792fca58231f203e21ac
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739479"
---
# <a name="voicecaption-property-commands-object"></a>Proprietà VoiceCaption (oggetto Commands)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta il testo visualizzato per l'oggetto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) nella finestra dei comandi vocali.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*Agent. ***Characters ("**_CharacterID_*_"). Stringa Commands. VoiceCaption_ *  \[  =  \]



| Parte     | Descrizione                                               |
|----------|-----------------------------------------------------------|
| *string* | Espressione stringa che restituisce il testo visualizzato. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Se si imposta la proprietà [**Voice**](voice-property.md) della raccolta [**Commands**](/windows/desktop/lwef/the-commands-collection-object) , in genere si imposta anche la relativa proprietà **VoiceCaption** . L'impostazione di testo **VoiceCaption** viene visualizzata nella finestra comandi vocali quando l'applicazione client è di tipo input-attivo e il carattere è visibile. Se questa proprietà non è impostata, l'impostazione per la proprietà [**Caption**](caption-property.md) della raccolta di **comandi** determina il testo visualizzato. Quando non viene impostata la proprietà **VoiceCaption** o **Caption** , i comandi della raccolta vengono visualizzati nella finestra comandi vocali in "(comando undefined)" quando l'applicazione client diventa input-Active.

L'impostazione **VoiceCaption** determina anche il testo visualizzato nel suggerimento di ascolto per indicare i comandi per i quali il carattere è in ascolto.

## <a name="see-also"></a>Vedere anche

[Proprietà Caption](caption-property.md)


 

 
