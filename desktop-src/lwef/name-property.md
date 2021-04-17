---
title: Proprietà Name (oggetto characters)
description: Proprietà Name
ms.assetid: vs|msagent|~\pacontrol_2bxm.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e7b4a8872952cce0ae68445ec22a5599891674
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474837"
---
# <a name="name-property-characters-object"></a>Proprietà Name (oggetto characters)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta una stringa che specifica il nome predefinito del carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("**_CharacterID_*_")._ *  \[  =  *Stringa* nome\]



| Parte     | Descrizione                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| *string* | Valore stringa corrispondente al nome del carattere (nell'impostazione della lingua corrente). |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Il **nome** di un carattere può dipendere dall'impostazione [**LanguageID**](languageid-property.md) del carattere. Il nome di un carattere in una lingua può essere diverso o usare caratteri diversi rispetto a un altro. Il **nome** predefinito del carattere per una lingua specifica viene definito quando il carattere viene compilato con l'editor dei caratteri di Microsoft Agent.

Evitare di rinominare un carattere, soprattutto quando viene usato in uno scenario in cui altre applicazioni client possono usare lo stesso carattere. Inoltre, Agent usa il **nome** del carattere per creare automaticamente i comandi per nascondere e visualizzare il carattere.

 

 




