---
description: Alcuni set di telefoni supportano la nozione di download o di caricamento dei dati nel dispositivo telefonico, che consente la programmazione del telefono in diversi modi.
ms.assetid: 5734107d-8104-4d8a-b3f7-3cc2a48f71ca
title: Aree dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81376549c63b4fcea92f705246cd58161faeac94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311910"
---
# <a name="data-areas"></a><span data-ttu-id="005ad-103">Aree dati</span><span class="sxs-lookup"><span data-stu-id="005ad-103">Data Areas</span></span>

<span data-ttu-id="005ad-104">Alcuni set di telefoni supportano la nozione di download o di caricamento dei dati nel dispositivo telefonico, che consente la programmazione del telefono in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="005ad-104">Some phone sets support the notion of downloading data from or uploading data to the phone device, which allows the phone set to be programmed in a variety of ways.</span></span> <span data-ttu-id="005ad-105">Questi set di telefono vengono modellati da TAPI con una o più aree di download o di caricamento.</span><span class="sxs-lookup"><span data-stu-id="005ad-105">TAPI models these phone sets as having one or more download or upload areas.</span></span> <span data-ttu-id="005ad-106">Ogni area è identificata da un numero compreso tra zero e il numero di aree dati disponibili sul telefono meno uno.</span><span class="sxs-lookup"><span data-stu-id="005ad-106">Each area is identified by a number that ranges from zero to the number of data areas available on the phone minus one.</span></span> <span data-ttu-id="005ad-107">Le dimensioni di ogni area possono variare.</span><span class="sxs-lookup"><span data-stu-id="005ad-107">Sizes of each area can vary.</span></span> <span data-ttu-id="005ad-108">Il formato dei dati è specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="005ad-108">The format of the data itself is device-specific.</span></span>

<span data-ttu-id="005ad-109">La funzione [**phoneSetData**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) di TAPI Scarica un buffer di dati in una determinata area dati del dispositivo telefonico e la funzione [**phoneGetData**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) carica il contenuto di una determinata area dati del dispositivo telefonico in un buffer.</span><span class="sxs-lookup"><span data-stu-id="005ad-109">The TAPI [**phoneSetData**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) function downloads a buffer of data to a given data area in the phone device, and the [**phoneGetData**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) function uploads the contents of a given data area in the phone device to a buffer.</span></span>

<span data-ttu-id="005ad-110">Quando viene modificata un'area dati di un dispositivo telefonico, all'applicazione viene inviato un messaggio di [**\_ stato telefonico**](phone-state.md) per notificare all'applicazione la modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="005ad-110">When a data area of a phone device is changed, a [**PHONE\_STATE**](phone-state.md) message is sent to the application to notify the application about the state change.</span></span> <span data-ttu-id="005ad-111">I parametri di questo messaggio forniscono un'indicazione della modifica.</span><span class="sxs-lookup"><span data-stu-id="005ad-111">Parameters to this message provide an indication of the change.</span></span>

 

 



