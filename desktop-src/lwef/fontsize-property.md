---
title: Proprietà FontSize (oggetto Commands)
description: Proprietà FontSize
ms.assetid: a1113a3a-5da8-4077-8565-168963c503d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee84d5eb966dd7d0605bd0e4f17674fe4499bab6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300848"
---
# <a name="fontsize-property-commands-object"></a>Proprietà FontSize (oggetto Commands)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta la dimensione del carattere utilizzata nel menu popup del carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*Agent. ***Characters ("**_CharacterID_*_"). Punti Commands. FontSize_ *  \[  =  \]



| Parte     | Descrizione                                              |
|----------|----------------------------------------------------------|
| *Punti* | Valore long integer che specifica la dimensione del carattere in punti. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La proprietà **FontSize** definisce la dimensione in punti del tipo di carattere utilizzato per visualizzare il testo nel menu popup del carattere. Il valore predefinito per l'impostazione del tipo di carattere è basato sull'impostazione del tipo di carattere del menu per l'impostazione **LanguageID** del carattere oppure, se non è impostato, l'impostazione della lingua predefinita dell'utente.

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

 

 




