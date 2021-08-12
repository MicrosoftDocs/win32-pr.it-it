---
title: Proprietà RaiseRequestErrors
description: Proprietà RaiseRequestErrors
ms.assetid: 60eb4478-526e-492a-8fb3-d1e54eff9868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081a47eef17378c24df5bdbcb0f5141b0dece45ec9933f289d0b3da9193793d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118246614"
---
# <a name="raiserequesterrors-property"></a>Proprietà RaiseRequestErrors

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta un valore che indica se vengono generati errori per le richieste.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Valore booleano RaiseRequestErrors* *  \[  =  \]



| Parte      | Descrizione                                                                                                                                                                                            |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Valore booleano che determina se vengono generati errori nelle richieste.<br/> **Vengono**    generati errori di richiesta True (impostazione predefinita). <br/> **False**     Gli errori di richiesta non vengono generati.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa proprietà consente di determinare se il server genera errori che si verificano con i metodi che supportano [**gli oggetti**](/windows/desktop/lwef/the-request-object) Request. Ad esempio, se si specifica un nome di animazione che non esiste in un metodo [**Play,**](play-method.md)il server genera un errore (visualizzando il messaggio di errore), a meno che non si imposta questa proprietà su **False**.

Può essere utile per i linguaggi di programmazione che non forniscono il ripristino quando viene generato un errore. Quando si imposta questa proprietà su **False,** tuttavia, è necessario fare attenzione perché potrebbe essere più difficile trovare errori nel codice.

 

