---
title: Proprietà Name (oggetto Characters)
description: Informazioni sulla proprietà Name dell'oggetto Characters. Microsoft Agent è deprecato a Windows 7.
ms.assetid: vs|msagent|~\pacontrol_2bxm.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e08509d5d2a349c56548259db4846203da6f632ff76c86309db87e6aa90583a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608651"
---
# <a name="name-property-characters-object"></a>Proprietà Name (oggetto Characters)

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

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

Il nome di un **carattere** può dipendere dall'impostazione [**LanguageID del**](languageid-property.md) carattere. Il nome di un carattere in una lingua può essere diverso o usare caratteri diversi rispetto a un altro. Il nome predefinito del carattere **per** una lingua specifica viene definito quando il carattere viene compilato con l'editor di caratteri di Microsoft Agent.

Evitare di rinominare un carattere, soprattutto quando viene utilizzato in uno scenario in cui altre applicazioni client possono usare lo stesso carattere. Agent usa anche il nome del carattere **per** creare automaticamente i comandi per nascondere e visualizzare il carattere.

 

 




