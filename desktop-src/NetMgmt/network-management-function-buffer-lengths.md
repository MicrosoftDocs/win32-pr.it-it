---
title: Lunghezze del buffer della funzione di gestione di rete
description: Questo argomento illustra i requisiti per le lunghezze del buffer di funzione quando viene usato con le API di gestione di rete.
ms.assetid: 08599966-68a1-420b-bbc7-6daac833d08f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5003f739d235a099adb9f4f403c15c67bd9169e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856233"
---
# <a name="network-management-function-buffer-lengths"></a><span data-ttu-id="1aa70-103">Lunghezze del buffer della funzione di gestione di rete</span><span class="sxs-lookup"><span data-stu-id="1aa70-103">Network Management Function Buffer Lengths</span></span>

<span data-ttu-id="1aa70-104">Questo argomento illustra i requisiti per le lunghezze del buffer di funzione quando viene usato con le API di gestione di rete.</span><span class="sxs-lookup"><span data-stu-id="1aa70-104">This topic discusses the requirements for function buffer lengths when used with the network management APIs.</span></span>

<span data-ttu-id="1aa70-105">Le applicazioni che specificano le dimensioni del buffer durante la chiamata di funzioni di enumerazione di gestione della rete (e varie funzioni di recupero dei dati) devono specificare buffer sufficientemente grandi da conservare la struttura o le strutture di informazioni restituite più le stringhe a cui puntano i membri.</span><span class="sxs-lookup"><span data-stu-id="1aa70-105">Applications that specify buffer sizes when calling network management enumeration functions (and various data retrieval functions) must specify buffers large enough to hold the returned information structure (or structures) plus the strings to which their members point.</span></span> <span data-ttu-id="1aa70-106">Se non si specifica un buffer sufficientemente grande per ricevere tutte le voci disponibili, la funzione restituisce l'errore di \_ altri \_ dati.</span><span class="sxs-lookup"><span data-stu-id="1aa70-106">If you do not specify a large enough buffer to receive all the available entries, the function returns ERROR\_MORE\_DATA.</span></span> <span data-ttu-id="1aa70-107">Le chiamate di enumerazione non restituiscono voci parziali.</span><span class="sxs-lookup"><span data-stu-id="1aa70-107">Enumeration calls do not return partial entries.</span></span>

<span data-ttu-id="1aa70-108">Alcune funzioni di gestione di rete accettano un parametro di lunghezza massima dei dati consultivo, *prefMaxLen*.</span><span class="sxs-lookup"><span data-stu-id="1aa70-108">Some network management functions take an advisory maximum data-length parameter, *prefmaxlen*.</span></span> <span data-ttu-id="1aa70-109">Questo parametro consente a un'applicazione di suggerire il numero di byte che il server deve restituire da una chiamata di funzione.</span><span class="sxs-lookup"><span data-stu-id="1aa70-109">This parameter allows an application to suggest the number of bytes the server should return from a function call.</span></span>

<span data-ttu-id="1aa70-110">Se si specifica la lunghezza massima \_ preferita del valore \_ nel parametro *prefMaxLen* , le funzioni di gestione della rete allocano la quantità di memoria necessaria per i dati.</span><span class="sxs-lookup"><span data-stu-id="1aa70-110">If you specify the value MAX\_PREFERRED\_LENGTH in the *prefmaxlen* parameter, the network management functions allocate the amount of memory required for the data.</span></span>

<span data-ttu-id="1aa70-111">Per ulteriori informazioni, vedere [buffer di funzioni di gestione di rete](network-management-function-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="1aa70-111">For more information, see [Network Management Function Buffers](network-management-function-buffers.md).</span></span>

 

 




