---
title: Creazione di dischi con più sessioni
description: IMAPi è in grado di creare dischi dati multisessione. Quando si crea un disco a più sessioni, è necessario tenere presenti alcune considerazioni.
ms.assetid: 02405a32-53d5-4618-bfa0-c9a9f5e3c51b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc41dba861ce29bd3d3e25e33ba0ba5ab5bf38a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221270"
---
# <a name="creating-discs-with-multiple-sessions"></a><span data-ttu-id="1e0f6-104">Creazione di dischi con più sessioni</span><span class="sxs-lookup"><span data-stu-id="1e0f6-104">Creating Discs with Multiple Sessions</span></span>

<span data-ttu-id="1e0f6-105">IMAPi è in grado di creare dischi dati multisessione.</span><span class="sxs-lookup"><span data-stu-id="1e0f6-105">IMAPI is capable of creating multi-session data discs.</span></span> <span data-ttu-id="1e0f6-106">Quando si crea un disco a più sessioni, è necessario tenere presenti alcune considerazioni.</span><span class="sxs-lookup"><span data-stu-id="1e0f6-106">There are a few considerations to be aware of when creating a multi-session disc.</span></span>

<span data-ttu-id="1e0f6-107">Il metodo [**IDiscMaster:: SetActiveDiscRecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder) determina se è presente un disco MULTIsessione IMAPI nell'unità attiva al momento dell'impostazione.</span><span class="sxs-lookup"><span data-stu-id="1e0f6-107">The [**IDiscMaster::SetActiveDiscRecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder) method determines whether there is an IMAPI multi-session disc in the active drive upon setting.</span></span> <span data-ttu-id="1e0f6-108">In tal caso, IMAPi passa automaticamente alla modalità multisessione.</span><span class="sxs-lookup"><span data-stu-id="1e0f6-108">If so, IMAPI goes into multi-session mode automatically.</span></span> <span data-ttu-id="1e0f6-109">L'uso di [**ClearFormatContent**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) dopo che è stata stabilita la modalità multisessione causa la restituzione di una modalità a sessione singola da parte di IMAPI.</span><span class="sxs-lookup"><span data-stu-id="1e0f6-109">Using [**ClearFormatContent**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) after multi-session mode has been established causes IMAPI to return to single-session mode.</span></span> <span data-ttu-id="1e0f6-110">Ciò significa che è necessario un disco vuoto per un'operazione di [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) Burn.</span><span class="sxs-lookup"><span data-stu-id="1e0f6-110">This means that a blank disc is required for a [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) burn.</span></span> <span data-ttu-id="1e0f6-111">Se il disco è in modalità multisessione, lo stesso disco deve trovarsi nel registratore attivo oppure verrà restituito un codice di errore IMAPi \_ e \_ WRONGDISC.</span><span class="sxs-lookup"><span data-stu-id="1e0f6-111">If the disc is in multi-session mode, the same disc must be in the active recorder or an error code of IMAPI\_E\_WRONGDISC will be returned.</span></span>

<span data-ttu-id="1e0f6-112">Selezionando un registratore nel formato Joliet, IMAPi leggerà le informazioni dal disco attualmente installato. Se il disco è un disco IMAPi Joliet precedente con spazio per un'altra sessione, IMAPi imposta automaticamente la modalità multisessione.</span><span class="sxs-lookup"><span data-stu-id="1e0f6-112">Selecting a recorder while in Joliet format causes IMAPI to read information from the currently installed disc. If the disc is a previous IMAPI Joliet disc that has space for another session, IMAPI automatically sets itself to multi-session mode.</span></span> <span data-ttu-id="1e0f6-113">Il disco deve essere presente nel registratore attivo quando si chiama [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc).</span><span class="sxs-lookup"><span data-stu-id="1e0f6-113">This disc must be present in the active recorder when calling [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc).</span></span>

<span data-ttu-id="1e0f6-114">La chiusura della prima sessione in un disco richiede 21 MB.</span><span class="sxs-lookup"><span data-stu-id="1e0f6-114">Closing the first session on a disc requires 21 MB.</span></span> <span data-ttu-id="1e0f6-115">Ogni sessione aggiuntiva richiede la chiusura di 11 MB.</span><span class="sxs-lookup"><span data-stu-id="1e0f6-115">Each additional session requires 11 MB to close.</span></span>

 

 




