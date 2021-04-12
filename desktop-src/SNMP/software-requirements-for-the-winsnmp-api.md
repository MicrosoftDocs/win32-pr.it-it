---
title: Requisiti software per l'API WinSNMP
description: Un'applicazione WinSNMP deve accedere all'API WinSNMP tramite la libreria a collegamento dinamico WSNMP32.DLL.
ms.assetid: ba0b9443-3fcf-41e2-993e-54e042f9d785
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31c30302f9f6d15cef221da46ce721dc4727a44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220903"
---
# <a name="software-requirements-for-the-winsnmp-api"></a><span data-ttu-id="44bbb-103">Requisiti software per l'API WinSNMP</span><span class="sxs-lookup"><span data-stu-id="44bbb-103">Software Requirements for the WinSNMP API</span></span>

<span data-ttu-id="44bbb-104">Un'applicazione WinSNMP deve accedere all'API WinSNMP tramite la libreria a collegamento dinamico WSNMP32.DLL.</span><span class="sxs-lookup"><span data-stu-id="44bbb-104">A WinSNMP application must access the WinSNMP API through the dynamic-link library WSNMP32.DLL.</span></span>

<span data-ttu-id="44bbb-105">I file seguenti sono necessari per supportare la funzionalità dell'API WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="44bbb-105">The following files are required to support the functionality of the WinSNMP API.</span></span>



| <span data-ttu-id="44bbb-106">Nome file</span><span class="sxs-lookup"><span data-stu-id="44bbb-106">Filename</span></span>     | <span data-ttu-id="44bbb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44bbb-107">Description</span></span>                                                                                  |
|--------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="44bbb-108">Wsnmp32. LIB</span><span class="sxs-lookup"><span data-stu-id="44bbb-108">WSNMP32.LIB</span></span>  | <span data-ttu-id="44bbb-109">Libreria WinSNMP</span><span class="sxs-lookup"><span data-stu-id="44bbb-109">WinSNMP Library</span></span>                                                                              |
| <span data-ttu-id="44bbb-110">WSNMP32.DLL</span><span class="sxs-lookup"><span data-stu-id="44bbb-110">WSNMP32.DLL</span></span>  | <span data-ttu-id="44bbb-111">Fornisce l'interfaccia WinSNMP</span><span class="sxs-lookup"><span data-stu-id="44bbb-111">Provides WinSNMP interface</span></span>                                                                   |
| <span data-ttu-id="44bbb-112">WINSNMP. H</span><span class="sxs-lookup"><span data-stu-id="44bbb-112">WINSNMP.H</span></span>    | <span data-ttu-id="44bbb-113">File di intestazione WinSNMP</span><span class="sxs-lookup"><span data-stu-id="44bbb-113">WinSNMP header file</span></span>                                                                          |
| <span data-ttu-id="44bbb-114">SNMPTRAP.EXE</span><span class="sxs-lookup"><span data-stu-id="44bbb-114">SNMPTRAP.EXE</span></span> | <span data-ttu-id="44bbb-115">Riceve trap SNMP e li inoltra al MGMTAPI.DLL, la libreria API Microsoft SNMP Manager</span><span class="sxs-lookup"><span data-stu-id="44bbb-115">Receives SNMP traps and forwards them to MGMTAPI.DLL, the Microsoft SNMP Manager API library</span></span> |
| <span data-ttu-id="44bbb-116">SNMPAPI.DLL</span><span class="sxs-lookup"><span data-stu-id="44bbb-116">SNMPAPI.DLL</span></span>  | <span data-ttu-id="44bbb-117">Fornisce utilità SNMP</span><span class="sxs-lookup"><span data-stu-id="44bbb-117">Provides SNMP utilities</span></span>                                                                      |



 

 

 




