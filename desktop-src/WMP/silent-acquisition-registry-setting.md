---
title: Impostazione del Registro di sistema acquisizione invisibile all'utente
description: Impostazione del Registro di sistema acquisizione invisibile all'utente
ms.assetid: 50e0b27e-ddf8-441f-adcd-d88d36f3edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bdab93c58dd92b5f0522f26ea192150cad4a44ae9a6edfbd0bde770f07a0262
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507961"
---
# <a name="silent-acquisition-registry-setting"></a>Impostazione del Registro di sistema acquisizione invisibile all'utente

Microsoft Windows Media Player il valore del Registro di sistema seguente per determinare se abilitare l'acquisizione invisibile all'utente, uno stato in cui il giocatore scarica automaticamente i diritti di utilizzo quando l'utente riproduce o sincronizza il contenuto protetto.

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** Preferenze \\ **di Microsoft** \\ **MediaPlayer** \\  \\ **SilentAcquisition**

Il formato del valore SilentAcquisition è il seguente:



| Nome              | Tipo           | Descrizione                                                                                                       |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------|
| SilentAcquisition | **REG \_ DWORD** | Impostare questo valore su 1 per abilitare l'acquisizione invisibile all'utente o su 0 per disabilitare l'acquisizione invisibile all'utente. Il valore predefinito è 1. |



 

Per specificare un valore, l'utente può  avviare Windows Media Player, aprire la finestra di dialogo Opzioni, fare clic sulla scheda **Privacy** e quindi selezionare o deselezionare la casella di controllo Scarica automaticamente i diritti di utilizzo durante la riproduzione o la sincronizzazione di un **file.** Se si seleziona questa casella di controllo, SilentAcquisition viene impostato su 1. se si deseleziona la casella di controllo, la proprietà viene impostata su 0.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Registro Impostazioni**](registry-settings.md)
</dt> </dl>

 

 




