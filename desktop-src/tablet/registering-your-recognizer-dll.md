---
description: Per usarlo, è necessario registrare la DLL del riconoscitore per la piattaforma Tablet PC. Il riconoscimento deve apportare le seguenti modifiche al registro di sistema al momento dell'installazione.
ms.assetid: 1f1d826b-3968-424b-8da8-b69590058ff1
title: Registrazione della DLL del riconoscitore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51114f11868e6d45dc4d319dab60e5b4f094ddbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530276"
---
# <a name="registering-your-recognizer-dll"></a><span data-ttu-id="4bf24-104">Registrazione della DLL del riconoscitore</span><span class="sxs-lookup"><span data-stu-id="4bf24-104">Registering Your Recognizer DLL</span></span>

<span data-ttu-id="4bf24-105">Per usarlo, è necessario registrare la DLL del riconoscitore per la piattaforma Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="4bf24-105">Your recognizer DLL must be registered for the Tablet PC Platform to use it.</span></span> <span data-ttu-id="4bf24-106">Il riconoscimento deve apportare le seguenti modifiche al registro di sistema al momento dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="4bf24-106">The recognizer must make the following changes to the registry at installation.</span></span>

<span data-ttu-id="4bf24-107">Aggiungere una nuova chiave per ognuno dei CLSID del riconoscimento sotto la \_ chiave del registro di sistema HKEY LOCAL \_ computer/software/Microsoft/TPG/Recognizers/Registry.</span><span class="sxs-lookup"><span data-stu-id="4bf24-107">Add a new key for each of the CLSIDs of your recognizer under the HKEY\_LOCAL\_MACHINE/SOFTWARE/Microsoft/TPG/Recognizers/ registry key.</span></span> <span data-ttu-id="4bf24-108">Aggiungere un solo CLSID per lingua.</span><span class="sxs-lookup"><span data-stu-id="4bf24-108">Add one CLSID per language.</span></span> <span data-ttu-id="4bf24-109">Nella tabella seguente vengono descritti i valori che devono essere aggiunti sotto ogni chiave contenente i CLSID.</span><span class="sxs-lookup"><span data-stu-id="4bf24-109">The following table describes the values that should be added underneath each of the keys containing your CLSIDs.</span></span>

> [!Note]  
> <span data-ttu-id="4bf24-110">I nomi di questi valori fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="4bf24-110">The names of these values are case sensitive.</span></span>

 



| <span data-ttu-id="4bf24-111">Nome del valore</span><span class="sxs-lookup"><span data-stu-id="4bf24-111">Value name</span></span>                             | <span data-ttu-id="4bf24-112">Tipo di valore</span><span class="sxs-lookup"><span data-stu-id="4bf24-112">Value type</span></span>             | <span data-ttu-id="4bf24-113">Descrizione del valore</span><span class="sxs-lookup"><span data-stu-id="4bf24-113">Value description</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bf24-114">Flag funzionalità di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="4bf24-114">Recognizer Capability Flags</span></span><br/> | <span data-ttu-id="4bf24-115">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="4bf24-115">REG\_DWORD</span></span><br/>  | <span data-ttu-id="4bf24-116">DWORD utilizzato per determinare le funzionalità del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="4bf24-116">DWORD used to determine the capabilities of the recognizer.</span></span><br/>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="4bf24-117">DLL di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="4bf24-117">Recognizer DLL</span></span><br/>              | <span data-ttu-id="4bf24-118">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="4bf24-118">REG\_SZ</span></span><br/>     | <span data-ttu-id="4bf24-119">Percorso completo della DLL del riconoscitore installato.</span><span class="sxs-lookup"><span data-stu-id="4bf24-119">Full path to the installed recognizer DLL.</span></span><br/>                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="4bf24-120">Lingue riconosciute</span><span class="sxs-lookup"><span data-stu-id="4bf24-120">Recognized Languages</span></span><br/>        | <span data-ttu-id="4bf24-121">REG \_ binario</span><span class="sxs-lookup"><span data-stu-id="4bf24-121">REG\_BINARY</span></span><br/> | <span data-ttu-id="4bf24-122">Matrice binaria che descrive la lingua o le lingue con cui un riconoscimento è progettato per funzionare.</span><span class="sxs-lookup"><span data-stu-id="4bf24-122">Binary array describing the language or languages that a recognizer is designed to work with.</span></span><br/> <span data-ttu-id="4bf24-123">In rictypes. h, il \_ numero massimo di lingue definito specifica il numero massimo di lingue supportate da un riconoscimento e ogni lingua accetta una parola da archiviare nell'elemento "lingue riconosciute".</span><span class="sxs-lookup"><span data-stu-id="4bf24-123">In rectypes.h, the MAX\_LANGUAGES define specifies the maximum number of languages supported by a recognizer, and each language takes a WORD to store in the "Recognized Languages" item.</span></span> <span data-ttu-id="4bf24-124">La dimensione della voce del \_ Registro di sistema reg Binary deve essere il numero massimo di \_ lingue \* sizeof (Word).</span><span class="sxs-lookup"><span data-stu-id="4bf24-124">The size of the REG\_BINARY registry entry should be MAX\_LANGUAGES \* sizeof(WORD).</span></span><br/> |



 

 

 




