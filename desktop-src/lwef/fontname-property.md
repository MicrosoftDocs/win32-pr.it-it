---
title: Proprietà FontName (oggetto Commands)
description: Fontname (proprietà)
ms.assetid: 7de3653e-9b4d-4a31-82d5-243f10e2743b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b04fa386958a75b55f9cfc50a9149de454d48f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118838"
---
# <a name="fontname-property-commands-object"></a>Proprietà FontName (oggetto Commands)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta il tipo di carattere utilizzato nel menu popup del carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*Agent. ***Characters ("**_CharacterID_*_")._ *  \[  =  *Tipo di carattere* Commands. fontname\]



| Parte   | Descrizione                                      |
|--------|--------------------------------------------------|
| *Carattere* | Valore stringa corrispondente al nome del tipo di carattere. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La proprietà **fontname** definisce il tipo di carattere utilizzato per visualizzare il testo nel menu popup del carattere. Il valore predefinito per l'impostazione del tipo di carattere è basato sull'impostazione del tipo di carattere del menu per l'impostazione **LanguageID** del carattere oppure--se non è impostato, ovvero l'impostazione dell'ID lingua predefinito dell'utente.

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

 

 




