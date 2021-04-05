---
title: Associazione a un oggetto ADSI
description: La connessione a un oggetto in un servizio directory è nota come binding.
ms.assetid: f3963019-9b3a-42d5-a978-484f294110e5
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, utilizzo, associazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c0fefcdb62d374d98e3007864168e2626ecc5d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707474"
---
# <a name="binding-to-an-adsi-object"></a><span data-ttu-id="26ebe-104">Associazione a un oggetto ADSI</span><span class="sxs-lookup"><span data-stu-id="26ebe-104">Binding to an ADSI Object</span></span>

<span data-ttu-id="26ebe-105">La connessione a un oggetto in un servizio directory è nota come binding.</span><span class="sxs-lookup"><span data-stu-id="26ebe-105">Connecting to an object in a directory service is known as binding.</span></span> <span data-ttu-id="26ebe-106">Il primo passaggio per la comunicazione con il sistema di directory sottostante è il binding a un oggetto ADSI.</span><span class="sxs-lookup"><span data-stu-id="26ebe-106">Binding to an ADSI object is the first step to communicating with the underlying directory system.</span></span> <span data-ttu-id="26ebe-107">Un oggetto deve essere associato a per spostarsi nello spazio dei nomi, cercare i dati, modificare i dati o rappresentare un utente.</span><span class="sxs-lookup"><span data-stu-id="26ebe-107">An object must be bound to in order to navigate its namespace, search for data, modify data, or impersonate a user.</span></span> <span data-ttu-id="26ebe-108">È anche possibile fornire caratteristiche di associazione aggiuntive, ad esempio nome utente, password, nome del server, metodi di crittografia e autenticazione protetta.</span><span class="sxs-lookup"><span data-stu-id="26ebe-108">It is also possible to supply additional binding characteristics, such as user name, password, server name, encryption methods, and secured authentication.</span></span> <span data-ttu-id="26ebe-109">Le caratteristiche di associazione aggiuntive effettive che è possibile utilizzare dipendono dal provider.</span><span class="sxs-lookup"><span data-stu-id="26ebe-109">The actual additional binding characteristics that can be used will depend on the provider.</span></span>

<span data-ttu-id="26ebe-110">Per ulteriori informazioni sull'associazione ADSI, vedere:</span><span class="sxs-lookup"><span data-stu-id="26ebe-110">For more information about ADSI binding, see:</span></span>

-   [<span data-ttu-id="26ebe-111">Stringa di binding</span><span class="sxs-lookup"><span data-stu-id="26ebe-111">Binding String</span></span>](binding-string.md)
-   [<span data-ttu-id="26ebe-112">Tipi di binding specifici per Active Directory</span><span class="sxs-lookup"><span data-stu-id="26ebe-112">Binding Types Specific to Active Directory</span></span>](binding-types-specific-to-active-directory.md)
-   [<span data-ttu-id="26ebe-113">Problemi di binding per ambienti misti</span><span class="sxs-lookup"><span data-stu-id="26ebe-113">Binding Issues for Mixed Environments</span></span>](binding-issues-for-mixed-environments.md)
-   [<span data-ttu-id="26ebe-114">Associazione a livello di codice tramite un'interfaccia ADSI</span><span class="sxs-lookup"><span data-stu-id="26ebe-114">Binding Programmatically Using an ADSI Interface</span></span>](binding-programmatically-using-an-adsi-interface.md)
-   [<span data-ttu-id="26ebe-115">Caching della connessione</span><span class="sxs-lookup"><span data-stu-id="26ebe-115">Connection Caching</span></span>](connection-caching.md)
-   [<span data-ttu-id="26ebe-116">Associazione a oggetti figlio</span><span class="sxs-lookup"><span data-stu-id="26ebe-116">Binding to Child Objects</span></span>](binding-to-child-objects.md)
-   [<span data-ttu-id="26ebe-117">Associazione all'elemento padre di un oggetto</span><span class="sxs-lookup"><span data-stu-id="26ebe-117">Binding to an Object's Parent</span></span>](binding-to-an-objectampaposs-parent.md)
-   [<span data-ttu-id="26ebe-118">Opzione di associazione rapida per le operazioni di scrittura/modifica batch</span><span class="sxs-lookup"><span data-stu-id="26ebe-118">Fast Binding Option for Batch Write/Modify Operations</span></span>](fast-binding-option-for-batch-writemodify-operations.md)
-   [<span data-ttu-id="26ebe-119">Scelta di un'interfaccia per l'associazione</span><span class="sxs-lookup"><span data-stu-id="26ebe-119">Choosing an Interface for Binding</span></span>](choosing-an-interface.md)

 

 




