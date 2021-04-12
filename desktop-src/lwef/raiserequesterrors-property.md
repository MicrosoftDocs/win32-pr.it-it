---
title: Proprietà RaiseRequestErrors
description: Proprietà RaiseRequestErrors
ms.assetid: 60eb4478-526e-492a-8fb3-d1e54eff9868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9e559f999db663a8a9f5874f6d16a10e1e78ac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104223859"
---
# <a name="raiserequesterrors-property"></a>Proprietà RaiseRequestErrors

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta un valore che indica se vengono generati errori per le richieste.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente * * *. RaiseRequestErrors*( *  \[  =  *booleano* )\]



| Parte      | Descrizione                                                                                                                                                                                            |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Valore booleano che determina se vengono generati errori nelle richieste.<br/> **True**    (impostazione predefinita) vengono generati errori di richiesta. <br/> **False**     Gli errori di richiesta non vengono generati.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa proprietà consente di determinare se il server genera errori che si verificano con i metodi che supportano gli oggetti [**richiesta**](/windows/desktop/lwef/the-request-object) . Se, ad esempio, si specifica un nome di animazione che non esiste in un metodo [**Play**](play-method.md), il server genera un errore (visualizzando il messaggio di errore), a meno che questa proprietà non venga impostata su **false**.

Può essere utile per i linguaggi di programmazione che non forniscono il ripristino quando viene generato un errore. Tuttavia, prestare attenzione quando si imposta questa proprietà su **false**, perché potrebbe essere più difficile trovare errori nel codice.

 

