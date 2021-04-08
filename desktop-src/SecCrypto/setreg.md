---
description: Lo strumento SetReg imposta il valore delle chiavi del registro di sistema che controllano il comportamento del processo di verifica del certificato Authenticode.
ms.assetid: 6c456a59-ee6c-420d-b075-7de8bd2fd8ff
title: SetReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05da29d3eddf7e04ba5bd735e1032f388d9d204a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749567"
---
# <a name="setreg"></a>SetReg

Lo strumento SetReg imposta il valore delle chiavi del registro di sistema che controllano il comportamento del processo di verifica del certificato Authenticode. Queste chiavi sono denominate chiavi di stato di pubblicazione software. Dopo aver completato l'azione richiesta, lo strumento Visualizza lo stato corrente delle chiavi dello stato di pubblicazione del software.

**Setreg** \[ *Opzioni* \] di \[ *Choice \#* {**true** \| **false**}\]

Lo strumento imposta Registro di sistema viene fornito solo con .NET Framework SDK versione 1,0 e 1,1, che è possibile scaricare dall' [area download Microsoft](https://www.microsoft.com/download/details.aspx?id=16217).

## <a name="options"></a>Opzioni

Le opzioni possono essere uno dei valori seguenti. Le opzioni fornite nella tabella seguente possono essere utilizzate solo con Internet Explorer 4,0 o versione successiva.



| Opzione | Descrizione                                                                                                                                            |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-q** | Consente di evitare la visualizzazione dei valori della chiave dello stato di pubblicazione del software dopo che SetReg ha completato l'azione richiesta. Per impostazione predefinita, i valori vengono visualizzati. |
| **-?** | Opzioni e sintassi del comando list.                                                                                                                       |



 

## <a name="choice-"></a>Scelta \#

*Scelta \#* deve essere uno dei valori seguenti.



| Scelta | Descrizione                                                                                                                       | Risultato                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------|-----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **1**  | Considerare attendibile la radice del test                                                                                                               | Questo valore viene ignorato. **Windows XP/2000:** Se **true**, considera attendibile una radice del test. Questa operazione equivale all'esecuzione di "regedit wvtston. reg" in Internet Explorer 3. *x*.<br/> Il valore predefinito è **false**. Tutti i file firmati con una radice di test non vengono verificati a meno che questo flag non sia impostato su **true**. Si noti che questo comportamento è stato modificato con Windows XP con Service Pack 1 (SP1) perché Windows XP con SP1 ignora questo valore.<br/> <br/> |
| **2**  | USA Data di scadenza per i certificati                                                                                               | Se **true**, controlla la data di scadenza del certificato. Per ignorare le date di scadenza, impostare questo flag su **false**. Il valore predefinito è **true**.                                                                                                                                                                                                                                                                                                       |
| **3**  | Controllare l' [ *elenco di revoche*](../secgloss/c-gly.md) | Se **true**, esegue il controllo di revoca. Per ignorare il controllo delle revoche, impostare questo flag su **false**. Il valore predefinito è **true**. **Internet Explorer 3. *x*:** il valore predefinito è **false**.<br/>                                                                                                                                                                                                                                               |
| **4**  | Server di revoca offline OK (singolo)<br/>                                                                              | Se **true**, consente l'approvazione offline per i singoli certificati. Il valore predefinito è **false**.                                                                                                                                                                                                                                                                                                                                                 |
| **5**  | Server di revoca offline OK (commerciale)<br/>                                                                              | Se **true**, consente l'approvazione offline per i certificati commerciali. Il valore predefinito è **true**.                                                                                                                                                                                                                                                                                                                                                  |
| **6**  | Server di revoca offline Java OK (singolo)<br/>                                                                         | Se **true**, consente l'approvazione offline per i singoli certificati e non Visualizza l'interfaccia utente per i certificati non validi. Il valore predefinito è **false**.                                                                                                                                                                                                                                                                                    |
| **7**  | Server di revoca offline Java OK (commerciale)<br/>                                                                         | Se **true**, consente l'approvazione offline per i certificati commerciali e non Visualizza l'interfaccia utente per i certificati non validi. Il valore predefinito è **true**.                                                                                                                                                                                                                                                                                     |
| **8**  | Rendere gli oggetti firmati della versione 1 non più validi                                                                                     | Se **true**, rende gli oggetti firmati della versione 1 non più validi. Il valore predefinito è **false**.                                                                                                                                                                                                                                                                                                                                                      |
| **9**  | Controllare l'elenco di revoche del server timestamp                                                                                | Se **true**, esegue il controllo delle revoche sul certificato del server del timestamp. Il valore predefinito è **false**. **Internet Explorer 3. *x*:** questo valore non è supportato.<br/>                                                                                                                                                                                                                                                            |
| **10** | Solo elementi attendibili trovati nel database Trust                                                                                      | Se **true**, consente il download dai publisher contenuti nel database di attendibilità personale. Il valore predefinito è **false**. **Internet Explorer 3. *x*:** questo valore non è supportato.<br/>                                                                                                                                                                                                                                             |



 

 

 
