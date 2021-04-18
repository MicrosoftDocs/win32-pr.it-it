---
title: Impostazione del registro di sistema acquisizione invisibile all'utente
description: Impostazione del registro di sistema acquisizione invisibile all'utente
ms.assetid: 50e0b27e-ddf8-441f-adcd-d88d36f3edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a00bbb6d930cb137ed12ffbcb05af31cee3c99c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298586"
---
# <a name="silent-acquisition-registry-setting"></a>Impostazione del registro di sistema acquisizione invisibile all'utente

Microsoft Windows Media Player utilizza il seguente valore del registro di sistema per determinare se abilitare l'acquisizione invisibile all'utente, uno stato in cui il lettore scarica automaticamente i diritti di utilizzo quando l'utente riproduce o Sincronizza il contenuto protetto.

**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **MediaPlayer** \\ **Preferences** \\ **SilentAcquisition**

Il valore di SilentAcquisition ha il formato seguente:



| Nome              | Tipo           | Descrizione                                                                                                       |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------|
| SilentAcquisition | **REG \_ DWORD** | Impostare questo valore su 1 per abilitare l'acquisizione invisibile all'utente o impostarlo su 0 per disabilitare l'acquisizione invisibile all'utente. Il valore predefinito è 1. |



 

Per specificare un valore, l'utente può avviare Media Player di Windows, aprire la finestra di dialogo **Opzioni** , fare clic sulla scheda **privacy** , quindi selezionare o deselezionare la casella di controllo **Scarica automaticamente i diritti di utilizzo quando si riproduce o si sincronizza un file** . Selezionando questa casella di controllo, si imposta SilentAcquisition su 1; Se si deseleziona la casella di controllo, questo viene impostato su 0.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Impostazioni del registro di sistema**](registry-settings.md)
</dt> </dl>

 

 




