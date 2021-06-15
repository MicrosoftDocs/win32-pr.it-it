---
title: Proprietà FontSize (oggetto Commands)
description: Informazioni sulla proprietà dell'oggetto Comandi FontSize. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: a1113a3a-5da8-4077-8565-168963c503d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05d4e32bf57d129e7bf1d7b45f97846a1fe90756
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068208"
---
# <a name="fontsize-property-commands-object"></a>Proprietà FontSize (oggetto Commands)

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta la dimensione del carattere utilizzata nel menu a comparsa del carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Commands.FontSize_ *  \[  =  *Points*\]



| Parte     | Descrizione                                              |
|----------|----------------------------------------------------------|
| *Punti* | Valore Long Integer che specifica la dimensione del carattere in punti. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La **proprietà FontSize** definisce le dimensioni in punti del tipo di carattere usato per visualizzare il testo nel menu a comparsa del carattere. Il valore predefinito per l'impostazione del tipo di carattere si basa sull'impostazione del tipo di carattere del menu per l'impostazione **LanguageID** del carattere o, se non è impostata, sull'impostazione della lingua predefinita dell'utente.

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

 

 




