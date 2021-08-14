---
title: Proprietà LanguageID
description: Proprietà LanguageID
ms.assetid: f57b0fa1-b3b8-49c8-b441-2a40e564d6ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13af9f7a508732444be83fd56cce2fad6c7d7a5c148e196e2c466db102d2e6e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118748699"
---
# <a name="languageid-property"></a>Proprietà LanguageID

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta l'ID lingua per il carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent.***Caratteri* *  **("**_CharacterID_*_"). LanguageID_* \[  =  *LanguageID*\]



Parte

Descrizione

LanguageID

Intero lungo che specifica l'ID lingua per il carattere. L'ID lingua (LANGID) per un carattere è un valore a 16 bit definito da Windows, costituito da un ID lingua primaria e un ID lingua secondaria. Gli esempi seguenti sono i valori per le lingue supportate da Microsoft Agent. Per determinare il valore per altri linguaggi, vedere la documentazione *di Platform SDK.*

 

Arabo

&H0401

Italiano

&H0410

 

Basco

&H042D

Giapponese

&H0411

 

Cinese (semplificato)

&H0804

Coreano

&H0412

 

Cinese (tradizionale)

&H0404

Norvegese

&H0414

 

Croato

&H041A

Polacco

&H0415

 

Ceco

&H0405

Portoghese (Portogallo)

&H0816

 

Danese

&H0406

Portoghese (Brasile)

&H0416

 

Olandese

&H0413

Romeno

&H0418

 

Inglese (Regno Unito)

&H0809

Russo

&H0419

 

Inglese (Stati Uniti)

&H0409

Slovacco

&H041B

 

Finlandese

&H040B

Sloveno

&H0424

 

Francese

&H040C

Spagnolo

&H0C0A

 

Tedesco

&H0407

Svedese

&H041D

 

Greco

&H0408

Thai

&H041E

 

Ebraico

&H040D

Turco

&H041F

 

Ungherese

&H040E

 

 



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Se non si imposta **LanguageID** per il carattere, il relativo ID lingua sarà l'ID lingua di sistema corrente se è installata la DLL della lingua dell'agente corrispondente. In caso contrario, la lingua del carattere sarà Inglese (Stati Uniti).

Questa proprietà determina anche la lingua per il testo del fumetto, i comandi nel menu a comparsa del carattere e il motore di riconoscimento vocale. Determina anche la lingua predefinita per l'output TTS.

Se si tenta di impostare **LanguageID** per un carattere e la DLL della lingua dell'agente per tale lingua non è installata o non è disponibile un tipo di carattere visualizzato per l'ID lingua, Agent genera un errore e **LanguageID** rimane all'ultima impostazione.

L'impostazione di questa proprietà non genera un errore se non sono presenti motori di riconoscimento vocale corrispondenti per la lingua. Per determinare se è disponibile un motore di riconoscimento vocale compatibile per **LanguageID,** controllare [**SRModeID**](srmodeid-property.md) o [**TTSModeID**](ttsmodeid-property.md). Se non si imposta **LanguageID,** verrà impostato sull'impostazione dell'ID lingua predefinita dell'utente.

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

> [!Note]  
> Se si imposta **LanguageID** su una lingua che supporta il testo bidirezionale (ad esempio arabo o ebraico), ma nel sistema che esegue l'applicazione non è installato il supporto bidirezionale, il testo nel fumetto della parola verrà visualizzato in ordine logico anziché di visualizzazione.

 

## <a name="see-also"></a>Vedere anche

[**Proprietà SRModeID**](srmodeid-property.md), [ **proprietà TTSModeID**](ttsmodeid-property.md)


 

 




