---
title: Informazioni sul driver di dispositivo
description: I driver e i moduli di dispositivo sono simili in quanto sono entrambi basati su file PE.
ms.assetid: 4f4ec15b-5592-4fe3-b754-fda25ab24159
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0735e791b8c6e1fc7434decc7ac71ccb5c1c469e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044338"
---
# <a name="device-driver-information"></a><span data-ttu-id="61b0e-103">Informazioni sul driver di dispositivo</span><span class="sxs-lookup"><span data-stu-id="61b0e-103">Device Driver Information</span></span>

<span data-ttu-id="61b0e-104">I driver e i moduli di dispositivo sono simili in quanto sono entrambi basati su file PE.</span><span class="sxs-lookup"><span data-stu-id="61b0e-104">Device drivers and modules are similar in that they are both based on PE files.</span></span> <span data-ttu-id="61b0e-105">Tuttavia, mentre ogni processo dispone di un proprio elenco privato di moduli caricati, i driver di dispositivo hanno moduli globali per il sistema.</span><span class="sxs-lookup"><span data-stu-id="61b0e-105">However, while each process has its own private list of loaded modules, device drivers have modules that are global to the system.</span></span> <span data-ttu-id="61b0e-106">Di conseguenza, PSAPI dispone di funzioni specifiche per ottenere l'elenco dei driver di dispositivo e i relativi nomi.</span><span class="sxs-lookup"><span data-stu-id="61b0e-106">Therefore, PSAPI has specific functions for obtaining the list of device drivers and their names.</span></span>

<span data-ttu-id="61b0e-107">È possibile recuperare l'indirizzo di caricamento per ogni driver di dispositivo chiamando la funzione [**EnumDeviceDrivers**](/windows/desktop/api/Psapi/nf-psapi-enumdevicedrivers) .</span><span class="sxs-lookup"><span data-stu-id="61b0e-107">You can retrieve the load address for each device driver by calling the [**EnumDeviceDrivers**](/windows/desktop/api/Psapi/nf-psapi-enumdevicedrivers) function.</span></span> <span data-ttu-id="61b0e-108">Questa funzione riempie una matrice di valori **LPVOID** con gli indirizzi di caricamento di tutti i driver di dispositivo nel sistema.</span><span class="sxs-lookup"><span data-stu-id="61b0e-108">This function fills an array of **LPVOID** values with the load addresses of all device drivers in the system.</span></span>

<span data-ttu-id="61b0e-109">La funzione [**GetDeviceDriverBaseName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverbasenamea) accetta un indirizzo di caricamento del driver come input e compila un buffer con il nome di base del driver, ad esempio Win32k.sys.</span><span class="sxs-lookup"><span data-stu-id="61b0e-109">The [**GetDeviceDriverBaseName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverbasenamea) function takes a driver load address as input and fills in a buffer with the base name of the driver (for example, Win32k.sys).</span></span> <span data-ttu-id="61b0e-110">Una funzione correlata, [**GetDeviceDriverFileName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverfilenamea), accetta gli stessi parametri e restituisce il percorso al driver di dispositivo (ad esempio, C: \\ Windows \\ system32 \\Win32k.sys).</span><span class="sxs-lookup"><span data-stu-id="61b0e-110">A related function, [**GetDeviceDriverFileName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverfilenamea), takes the same parameters and returns the path to the device driver (for example, C:\\Windows\\System32\\Win32k.sys).</span></span>

 

 




