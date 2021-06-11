---
title: Proprietà Name (oggetto Characters)
description: Informazioni sulla proprietà Name dell'oggetto Characters. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: vs|msagent|~\pacontrol_2bxm.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7365550d5d4d4071cf4292e505f16e7047628cf1
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989326"
---
# <a name="name-property-characters-object"></a>Proprietà Name (oggetto Characters)

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta una stringa che specifica il nome predefinito del carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Stringa del_ *  \[  =  *nome*\]



| Parte     | Descrizione                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| *string* | Valore stringa corrispondente al nome del carattere (nell'impostazione della lingua corrente). |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Il nome di un **carattere** può dipendere dall'impostazione [**LanguageID del**](languageid-property.md) carattere. Il nome di un carattere in una lingua può essere diverso o usare caratteri diversi rispetto a in un'altra. Il nome predefinito **del** carattere per una lingua specifica viene definito quando il carattere viene compilato con Microsoft Agent Character Editor.

Evitare di rinominare un carattere, soprattutto quando lo si usa in uno scenario in cui altre applicazioni client possono usare lo stesso carattere. Agent usa anche il nome del **carattere** per creare automaticamente i comandi per nascondere e visualizzare il carattere.

 

 




