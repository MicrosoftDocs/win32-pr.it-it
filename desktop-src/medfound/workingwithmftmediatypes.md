---
description: Uso dei tipi di supporto MFT
ms.assetid: 16c270ee-f246-4222-97e9-d8d0fe009155
title: Uso dei tipi di supporto MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98bfc996704f6069ca1d16570b33f456ea1cc115
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104234482"
---
# <a name="working-with-mft-media-types"></a><span data-ttu-id="d9efa-103">Uso dei tipi di supporto MFT</span><span class="sxs-lookup"><span data-stu-id="d9efa-103">Working with MFT Media Types</span></span>

<span data-ttu-id="d9efa-104">Un tipo di supporto è un modo per descrivere il formato di un flusso multimediale.</span><span class="sxs-lookup"><span data-stu-id="d9efa-104">A media type is a way to describe the format of a media stream.</span></span> <span data-ttu-id="d9efa-105">In Media Foundation i tipi di supporto sono rappresentati dall'interfaccia **IMFMediaType** .</span><span class="sxs-lookup"><span data-stu-id="d9efa-105">In Media Foundation, media types are represented by the **IMFMediaType** interface.</span></span> <span data-ttu-id="d9efa-106">Questa interfaccia eredita l'interfaccia **IMFAttributes** .</span><span class="sxs-lookup"><span data-stu-id="d9efa-106">This interface inherits the **IMFAttributes** interface.</span></span> <span data-ttu-id="d9efa-107">I dettagli di un tipo di supporto vengono specificati come attributi.</span><span class="sxs-lookup"><span data-stu-id="d9efa-107">The details of a media type are specified as attributes.</span></span>

<span data-ttu-id="d9efa-108">Per creare un nuovo tipo di supporto, chiamare la funzione **MFCreateMediaType** .</span><span class="sxs-lookup"><span data-stu-id="d9efa-108">To create a new media type, call the **MFCreateMediaType** function.</span></span> <span data-ttu-id="d9efa-109">Questa funzione restituisce un puntatore all'interfaccia **IMFMediaType** .</span><span class="sxs-lookup"><span data-stu-id="d9efa-109">This function returns a pointer to the **IMFMediaType** interface.</span></span> <span data-ttu-id="d9efa-110">Il tipo di supporto inizialmente non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="d9efa-110">The media type initially has no attributes.</span></span>

<span data-ttu-id="d9efa-111">Il Media Foundation SDK fornisce diverse funzioni di supporto per l'inizializzazione di tipi di supporto da strutture di formato.</span><span class="sxs-lookup"><span data-stu-id="d9efa-111">The Media Foundation SDK provides several helper functions for initializing Media Types from format structures.</span></span> <span data-ttu-id="d9efa-112">Ad esempio, la funzione **MFInitMediaTypeFromVideoInfoHeader** Inizializza un tipo di video da una struttura **VIDEOINFOHEADER** e la funzione **MFInitMediaTypeFromWaveFormatEx** Inizializza un tipo di video da una struttura **WAVEFORMATEX** o **WAVEFORMATEXTENSIBLE** .</span><span class="sxs-lookup"><span data-stu-id="d9efa-112">For example the function **MFInitMediaTypeFromVideoInfoHeader** initializes a video type from a **VIDEOINFOHEADER** structure, and the function **MFInitMediaTypeFromWaveFormatEx** initializes a video type from a **WAVEFORMATEX** or **WAVEFORMATEXTENSIBLE** structure.</span></span>

<span data-ttu-id="d9efa-113">I tipi di formato usati dai codec sono generalmente limitati a quelli descritti dalle strutture **VIDEOINFOHEADER** e **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="d9efa-113">The format types that are used by the codecs are generally limited to those described by the **VIDEOINFOHEADER** and **WAVEFORMATEX** structures.</span></span>

<span data-ttu-id="d9efa-114">Altre informazioni sulla creazione e l'accesso a Media Foundation tipi di supporto sono disponibili nella documentazione di Media Foundation SDK.</span><span class="sxs-lookup"><span data-stu-id="d9efa-114">More information on creating and accessing Media Foundation media types is available in the Media Foundation SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9efa-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d9efa-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9efa-116">Uso di codec MFTs</span><span class="sxs-lookup"><span data-stu-id="d9efa-116">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



