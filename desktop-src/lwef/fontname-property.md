---
title: Proprietà FontName (oggetto Commands)
description: Informazioni sulla proprietà dell'oggetto Comandi FontName. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: 7de3653e-9b4d-4a31-82d5-243f10e2743b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 739fceae4e73788f408306f6af08713173c99843
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068257"
---
# <a name="fontname-property-commands-object"></a>Proprietà FontName (oggetto Commands)

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta il tipo di carattere utilizzato nel menu a comparsa del carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Tipo di carattere Commands.FontName_ *  \[  =  \]



| Parte   | Descrizione                                      |
|--------|--------------------------------------------------|
| *Carattere* | Valore stringa corrispondente al nome del tipo di carattere. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La **proprietà FontName** definisce il tipo di carattere usato per visualizzare il testo nel menu a comparsa del carattere. Il valore predefinito per l'impostazione del tipo di carattere si basa sull'impostazione del tipo di carattere del menu per l'impostazione **LanguageID** del carattere oppure, se non è impostata, sull'impostazione dell'ID lingua predefinita dell'utente.

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. L'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

 

 




