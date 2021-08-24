---
description: La tecnica a livello di codice consigliata per l'impostazione di contesti in un'applicazione non abilitata per l'input penna consiste nell'usare le funzioni SetInputScope per associare il contesto ai campi nell'applicazione.
ms.assetid: 95b93804-8079-4b97-b1b0-dfc0138c94e8
title: Impostazione del contesto con le API SetInputScope
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0abe9992e4a4ee81190fdee022b11f443592e05d7c99f9a5e69d0a200f63ecbf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708151"
---
# <a name="setting-context-with-the-setinputscope-apis"></a>Impostazione del contesto con le API SetInputScope

La tecnica a livello di codice consigliata per l'impostazione di contesti in un'applicazione non abilitata per l'input penna consiste nell'usare le [**funzioni SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) per associare il contesto ai campi nell'applicazione.

Microsoft Windows XP Tablet PC Edition Development Kit 1.7 è stata la prima versione di Microsoft Windows per offrire [**SetInputScope.**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) Windows Vista fornisce anche il supporto per queste funzioni. Le **definizioni SetInputScope** sono dichiarate in InputScope.idl e InputScope.h. Per altre informazioni, [vedere](../tsf/text-services-framework.md)Framework servizi di testo .

Le [**funzioni SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) sono il modo consigliato per impostare il contesto per i controlli e le applicazioni non abilitate per l'input penna.

## <a name="common-input-scopes"></a>Ambiti di input comuni

Usando le [**funzioni SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) e il set definito di ambiti di input comuni descritti nell'enumerazione [**InputScope,**](/windows/win32/api/inputscope/ne-inputscope-inputscope) è possibile migliorare l'accuratezza del riconoscimento della grafia Microsoft.

> [!Note]  
> I riconoscitori per inglese (Stati Uniti), inglese (Regno Unito), tedesco, francese, italiano, spagnolo, olandese e portoghese attualmente supportano l'uso degli ambiti di input comuni con [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).

 

 

 
