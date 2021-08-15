---
description: Lo strumento SetReg imposta il valore delle chiavi del Registro di sistema che controllano il comportamento del processo di verifica del certificato Authenticode.
ms.assetid: 6c456a59-ee6c-420d-b075-7de8bd2fd8ff
title: SetReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5267aa140cad713e550ddf8afd0281d489bdd90ac0b26a7f7a4781240ecac24c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900301"
---
# <a name="setreg"></a>SetReg

Lo strumento SetReg imposta il valore delle chiavi del Registro di sistema che controllano il comportamento del processo di verifica del certificato Authenticode. Queste chiavi sono denominate chiavi di stato di pubblicazione software. Dopo aver completato l'azione richiesta, lo strumento visualizza lo stato corrente delle chiavi di stato di pubblicazione software.

**SetReg** \[ *Opzioni* \] \[ *Choice \#* {**TRUE** \| **FALSE**}\]

Lo strumento Set Registry viene fornito solo con .NET Framework SDK versione 1.0 e .1.1, scaricabile [dall'Area download Microsoft.](https://www.microsoft.com/download/details.aspx?id=16217)

## <a name="options"></a>Opzioni

Le opzioni possono essere uno dei valori seguenti. Le opzioni specificate nella tabella seguente possono essere usate solo con Internet Explorer 4.0 o versione successiva.



| Opzione | Descrizione                                                                                                                                            |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-q** | Eliminare la visualizzazione dei valori della chiave di stato di pubblicazione software dopo che SetReg ha completato l'azione richiesta. I valori vengono visualizzati per impostazione predefinita. |
| **-?** | Elencare la sintassi e le opzioni dei comandi.                                                                                                                       |



 

## <a name="choice-"></a>Scelta \#

*Scelta \#* deve essere uno dei valori seguenti.



| Scelta | Descrizione                                                                                                                       | Risultato                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------|-----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **1**  | Considerare attendibile la radice di test                                                                                                               | Questo valore viene ignorato. **Windows XP/2000:** Se **TRUE,** considera attendibile una radice di test. Equivale all'esecuzione di "regedit wvtston.reg" in Internet Explorer 3. *x*.<br/> Il valore predefinito è **FALSE.** Qualsiasi file firmato con una radice di test non verificherà a meno che questo flag non sia impostato su **TRUE.** Si noti che questo comportamento è stato modificato con Windows XP con Service Pack 1 (SP1) perché Windows XP con SP1 ignora questo valore.<br/> <br/> |
| **2**  | Usare la data di scadenza per i certificati                                                                                               | Se **TRUE,** controlla la data di scadenza del certificato. Per ignorare le date di scadenza, impostare questo flag su **FALSE.** Il valore predefinito è **TRUE.**                                                                                                                                                                                                                                                                                                       |
| **3**  | Controllare [ *l'elenco di revoche*](../secgloss/c-gly.md) | Se **TRUE,** esegue il controllo di revoca. Per ignorare il controllo delle revoche, impostare questo flag su **FALSE.** Il valore predefinito è **TRUE.** **Internet Explorer 3. *x*: il** valore predefinito è **FALSE.**<br/>                                                                                                                                                                                                                                               |
| **4**  | Server di revoca offline OK (singolo)<br/>                                                                              | Se **TRUE,** consente l'approvazione offline per singoli certificati. Il valore predefinito è **FALSE.**                                                                                                                                                                                                                                                                                                                                                 |
| **5**  | Server di revoca offline OK (commerciale)<br/>                                                                              | Se **TRUE,** consente l'approvazione offline per i certificati commerciali. Il valore predefinito è **TRUE.**                                                                                                                                                                                                                                                                                                                                                  |
| **6**  | Server di revoca offline Java OK (singolo)<br/>                                                                         | Se **TRUE,** consente l'approvazione offline per i singoli certificati e non visualizza l'interfaccia utente per i certificati non validi. Il valore predefinito è **FALSE.**                                                                                                                                                                                                                                                                                    |
| **7**  | Server di revoca offline Java OK (commerciale)<br/>                                                                         | Se **TRUE,** consente l'approvazione offline per i certificati commerciali e non visualizza l'interfaccia utente per i certificati non validi. Il valore predefinito è **TRUE.**                                                                                                                                                                                                                                                                                     |
| **8**  | Rendere gli oggetti firmati versione 1 non più validi                                                                                     | Se **TRUE,** rende gli oggetti firmati versione 1 non più validi. Il valore predefinito è **FALSE.**                                                                                                                                                                                                                                                                                                                                                      |
| **9**  | Controllare l'elenco di revoche del server di timestamp                                                                                | Se **TRUE,** esegue il controllo di revoca sul certificato del server timestamp. Il valore predefinito è **FALSE.** **Internet Explorer 3. *x*:** questo valore non è supportato.<br/>                                                                                                                                                                                                                                                            |
| **10** | Solo gli elementi attendibili trovati nel database attendibilità                                                                                      | Se **TRUE,** consente i download dagli editori contenuti nel database di attendibilità personale. Il valore predefinito è **FALSE.** **Internet Explorer 3. *x*:** questo valore non è supportato.<br/>                                                                                                                                                                                                                                             |



 

 

 
