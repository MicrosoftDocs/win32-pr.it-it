---
description: La tecnica di programmazione consigliata per l'impostazione di contesti in un'applicazione che non è abilitata per l'input penna consiste nell'utilizzare le funzioni SetInputScope per associare il contesto ai campi nell'applicazione.
ms.assetid: 95b93804-8079-4b97-b1b0-dfc0138c94e8
title: Impostazione del contesto con le API SetInputScope
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c1b507b1719bea8c04288dca9214ad5675f8a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313914"
---
# <a name="setting-context-with-the-setinputscope-apis"></a>Impostazione del contesto con le API SetInputScope

La tecnica di programmazione consigliata per l'impostazione di contesti in un'applicazione che non è abilitata per l'input penna consiste nell'utilizzare le funzioni [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) per associare il contesto ai campi nell'applicazione.

Microsoft Windows XP Tablet PC Edition Development Kit 1,7 è stata la prima versione di Microsoft Windows a offrire [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope). Windows Vista fornisce anche il supporto per queste funzioni. Le definizioni **SetInputScope** sono dichiarate in InputScope. idl e InputScope. h. Per altre informazioni, vedere [Framework di servizi di testo](../tsf/text-services-framework.md).

Le funzioni [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) rappresentano la modalità consigliata per impostare il contesto per i controlli e le applicazioni che non sono abilitati per l'input penna.

## <a name="common-input-scopes"></a>Ambiti di input comuni

Utilizzando le funzioni [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) e il set definito di ambiti di input comuni descritti nell'enumerazione [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) , è possibile migliorare l'accuratezza del riconoscimento dei riconoscitori della grafia Microsoft.

> [!Note]  
> I riconoscitori per la lingua inglese (Stati Uniti), inglese (Regno Unito), tedesco, francese, italiano, spagnolo, olandese e portoghese attualmente supportano l'utilizzo degli ambiti di input comuni con [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).

 

 

 
