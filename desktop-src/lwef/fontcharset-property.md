---
title: Proprietà FontCharSet
description: Proprietà FontCharSet
ms.assetid: 2f23a242-d620-4766-8f59-cf158aa55969
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4561de9af823b4213266a93b7bfa2e29588c3c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331951"
---
# <a name="fontcharset-property"></a>Proprietà FontCharSet

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta il set di caratteri per il tipo di carattere visualizzato nell'aerostato di parola del carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("*** CharacterID * * *"). Valore di Balloon. FontCharSet* *  \[  =  \]



| Parte    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *value* | Valore intero che specifica il set di caratteri utilizzato dal tipo di carattere. Di seguito sono riportate alcune impostazioni comuni per valore: 0 caratteri Windows standard (ANSI).<br/> 1 set di caratteri predefinito.<br/> 2 il set di caratteri del simbolo.<br/> 128 DBCS (Double byte character set) univoco per la versione giapponese di Windows.<br/> 129 DBCS (Double byte character set) univoco per la versione coreana di Windows.<br/> 134 DBCS (Double byte character set) univoco per la versione in cinese semplificato di Windows.<br/> 136 DBCS (Double byte character set) univoco per la versione cinese tradizionale di Windows.<br/> 255 caratteri estesi normalmente visualizzati dalle applicazioni Microsoft MS-DOS.<br/> Per altri valori del set di caratteri, vedere la documentazione di Platform SDK.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Il valore predefinito per il set di caratteri del fumetto di parole di un carattere viene impostato nell'editor dei caratteri di Microsoft Agent. Inoltre, l'utente può eseguire l'override delle impostazioni del set di caratteri per tutti i caratteri nella finestra delle proprietà di Microsoft Agent.

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

> [!Note]  
> Se si usa un carattere non compilato, controllare le proprietà [**fontname**](fontname-property.md) e **FontCharSet** per il carattere per determinare se sono appropriate per le impostazioni locali. Potrebbe essere necessario impostare questi valori prima di utilizzare il metodo [**Speak**](speak-method.md) per garantire la visualizzazione del testo appropriata all'interno del fumetto di Word.

 

## <a name="see-also"></a>Vedere anche

[**Fontname (proprietà)**](fontname-property.md)


 

 





