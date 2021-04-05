---
description: È possibile definire gli ambiti di input personalizzati usando modelli di linguaggio composte da espressioni regolari per la grafia e assegnando loro i campi. Se, ad esempio, si crea un'applicazione di database per le parti del magazzino e si desidera che gli utenti siano in grado di immettere numeri di parte utilizzando il riquadro di scrittura del pannello di input di Tablet PC. Se la sintassi del numero di parte è costituita da tre lettere seguite da quattro numeri seguiti da un'altra lettera (ad esempio, ABC1234D), il riconoscimento della grafia potrebbe avere un tempo difficile per riconoscere tale input perché non è definito nel modello di linguaggio. Non esiste alcun controllo del controllo predefinito corrispondente a tale sintassi, né Microsoft può includere la sintassi per ogni possibile campo che potrebbe essere necessario per un'applicazione. Le espressioni regolari di grafia consentono alle applicazioni di definire in modo semplice un modello di linguaggio specifico per un particolare campo di utilizzo speciale. Nota Quando si lavora in un'applicazione abilitata per l'input penna che usa la proprietà del controllo dell'oggetto RecognizerContext, non è possibile usare la versione 1 factoids in un'espressione regolare.
ms.assetid: 71f80196-0a36-4a14-a115-712bc909f6d7
title: Ambiti di input personalizzati con espressioni regolari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bdd7807221aca7b05ed4dc1facf7ddb01470c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049294"
---
# <a name="custom-input-scopes-with-regular-expressions"></a><span data-ttu-id="43bd9-106">Ambiti di input personalizzati con espressioni regolari</span><span class="sxs-lookup"><span data-stu-id="43bd9-106">Custom Input Scopes with Regular Expressions</span></span>

<span data-ttu-id="43bd9-107">È possibile definire gli ambiti di input personalizzati usando modelli di linguaggio composte da espressioni regolari per la grafia e assegnando loro i campi.</span><span class="sxs-lookup"><span data-stu-id="43bd9-107">You can define custom input scopes by using language models composed of regular expressions for handwriting and assigning them to fields.</span></span>

<span data-ttu-id="43bd9-108">Se, ad esempio, si crea un'applicazione di database per le parti del magazzino e si desidera che gli utenti siano in grado di immettere numeri di parte utilizzando il riquadro di scrittura del pannello di input di Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="43bd9-108">For example, if you are creating a database application for warehouse parts and want users to be able to enter part numbers using the Tablet PC Input Panel's writing pad.</span></span> <span data-ttu-id="43bd9-109">Se la sintassi del numero di parte è costituita da tre lettere seguite da quattro numeri seguiti da un'altra lettera (ad esempio, ABC1234D), il riconoscimento della grafia potrebbe avere un tempo difficile per riconoscere tale input perché non è definito nel modello di linguaggio.</span><span class="sxs-lookup"><span data-stu-id="43bd9-109">If the part number syntax consists of three letters followed by four numbers followed by another letter (for example, ABC1234D), the handwriting recognizer would have a difficult time recognizing such input because it is not defined in the language model.</span></span> <span data-ttu-id="43bd9-110">Non esiste alcun controllo del controllo predefinito corrispondente a tale sintassi, né Microsoft può includere la sintassi per ogni possibile campo che potrebbe essere necessario per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="43bd9-110">There is no predefined factoid that corresponds to such syntax, nor can Microsoft include the syntax for every possible field an application might need.</span></span> <span data-ttu-id="43bd9-111">Le espressioni regolari di grafia consentono alle applicazioni di definire in modo semplice un modello di linguaggio specifico per un particolare campo di utilizzo speciale.</span><span class="sxs-lookup"><span data-stu-id="43bd9-111">Handwriting regular expressions provide an easy way for applications to define their own language model for a particular special-use field.</span></span>

> [!Note]  
> <span data-ttu-id="43bd9-112">Quando si lavora in un'applicazione abilitata per l'input penna che [**Usa la proprietà del controllo**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) dell'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) , non è possibile usare la versione 1 factoids in un'espressione regolare.</span><span class="sxs-lookup"><span data-stu-id="43bd9-112">When working in an ink-enabled application that uses the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property of the [**RecognizerContext**](inkrecognizercontext-class.md) object, you cannot use version 1 factoids in a regular expression.</span></span>

 

 

 



