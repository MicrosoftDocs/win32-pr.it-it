---
title: Attributi multipoint in WSAPROTOCOL_INFO
description: Gli attributi multipoint nella struttura delle informazioni di WSAPROTOCOL \_ includono il \_ supporto di XP1 \_ MultiPoint, il \_ \_ piano di controllo multipoint XP1 e il \_ \_ \_ piano dati multipoint XP1 \_ .
ms.assetid: f1bd5aa1-e705-4eaf-9436-fed0ea03f113
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baedcd07f53db462eb090217b53d93a1a4aa8c34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751439"
---
# <a name="multipoint-attributes-in-wsaprotocol_info"></a><span data-ttu-id="a3267-103">Attributi multipoint in WSAPROTOCOL_INFO</span><span class="sxs-lookup"><span data-stu-id="a3267-103">Multipoint attributes in WSAPROTOCOL_INFO</span></span>

<span data-ttu-id="a3267-104">Tre parametri di attributo sono definiti nella struttura delle [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per distinguere i diversi schemi utilizzati rispettivamente nel controllo e nei piani dati:</span><span class="sxs-lookup"><span data-stu-id="a3267-104">Three attribute parameters are defined in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure in order to distinguish the different schemes used in the control and data planes, respectively:</span></span>

-   <span data-ttu-id="a3267-105">XP1 \_ supporta \_ multipoint con un valore 1 indica che questa voce di protocollo supporta le comunicazioni multipoint e che i due parametri seguenti sono significativi.</span><span class="sxs-lookup"><span data-stu-id="a3267-105">XP1\_SUPPORT\_MULTIPOINT with a value of 1 indicates this protocol entry supports multipoint communications, and that the following two parameters are meaningful.</span></span>
-   <span data-ttu-id="a3267-106">\_ \_ \_ Il piano di controllo multipoint XP1 indica se il piano di controllo è radice (valore = 1) o non radice (valore = 0).</span><span class="sxs-lookup"><span data-stu-id="a3267-106">XP1\_MULTIPOINT\_CONTROL\_PLANE indicates whether the control plane is rooted (value = 1) or nonrooted (value = 0).</span></span>
-   <span data-ttu-id="a3267-107">\_ \_ Il piano dati multipoint XP1 \_ indica se il piano dati è radice (valore = 1) o non radice (valore = 0).</span><span class="sxs-lookup"><span data-stu-id="a3267-107">XP1\_MULTIPOINT\_DATA\_PLANE indicates whether the data plane is rooted (value = 1) or nonrooted (value = 0).</span></span>

<span data-ttu-id="a3267-108">Sono presenti due voci di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) se un protocollo multipoint supporta i piani dati radice e non radice, una voce per ogni.</span><span class="sxs-lookup"><span data-stu-id="a3267-108">Two [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entries would be present if a multipoint protocol supported both rooted and nonrooted data planes, one entry for each.</span></span>

 

 
