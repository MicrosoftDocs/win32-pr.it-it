---
title: Codici di errore LDAP per ADSI
description: Quando un server LDAP genera un errore e passa l'errore al client, l'errore viene quindi convertito in una stringa dal client LDAP.
ms.assetid: 7a0a5a1b-8473-405b-a590-3f917e50cbdc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149abf4562b0e35067149fb69c9a1ec1304cc528
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855285"
---
# <a name="ldap-error-codes-for-adsi"></a><span data-ttu-id="74dd6-103">Codici di errore LDAP per ADSI</span><span class="sxs-lookup"><span data-stu-id="74dd6-103">LDAP Error Codes for ADSI</span></span>

<span data-ttu-id="74dd6-104">Quando un server LDAP genera un errore e passa l'errore al client, l'errore viene quindi convertito in una stringa dal client LDAP.</span><span class="sxs-lookup"><span data-stu-id="74dd6-104">When an LDAP server generates an error and passes the error to the client, the error is then translated into a string by the LDAP client.</span></span>

<span data-ttu-id="74dd6-105">Questo metodo è simile ai [codici di errore Win32 per ADSI](win32-error-codes-for-adsi.md).</span><span class="sxs-lookup"><span data-stu-id="74dd6-105">This method is similar to [Win32 error codes for ADSI](win32-error-codes-for-adsi.md).</span></span> <span data-ttu-id="74dd6-106">In questo esempio, il codice di errore del client è l'errore WIN32 0x80072020.</span><span class="sxs-lookup"><span data-stu-id="74dd6-106">In this example, the client error code is the WIN32 error 0x80072020.</span></span>

<span data-ttu-id="74dd6-107">**Per determinare i codici di errore LDAP per ADSI**</span><span class="sxs-lookup"><span data-stu-id="74dd6-107">**To Determine the LDAP error codes for ADSI**</span></span>

1.  <span data-ttu-id="74dd6-108">Eliminare 8007 dal codice di errore WIN32.</span><span class="sxs-lookup"><span data-stu-id="74dd6-108">Drop the 8007 from the WIN32 error code.</span></span> <span data-ttu-id="74dd6-109">Nell'esempio, il valore esadecimale rimanente è 2020.</span><span class="sxs-lookup"><span data-stu-id="74dd6-109">In the example, the remaining hex value is 2020.</span></span>
2.  <span data-ttu-id="74dd6-110">Converte il valore esadecimale rimanente in un valore decimale.</span><span class="sxs-lookup"><span data-stu-id="74dd6-110">Convert the remaining hex value to a decimal value.</span></span> <span data-ttu-id="74dd6-111">Nell'esempio, il valore esadecimale rimanente 2020 viene convertito nel valore decimale 8224.</span><span class="sxs-lookup"><span data-stu-id="74dd6-111">In the example, the remaining hex value 2020 converts to the decimal value 8224.</span></span>
3.  <span data-ttu-id="74dd6-112">Cercare nel file WinError. h la definizione del valore decimale.</span><span class="sxs-lookup"><span data-stu-id="74dd6-112">Search in the WinError.h file for the definition of the decimal value.</span></span> <span data-ttu-id="74dd6-113">Nell'esempio, 8224L corrisponde all'errore di **\_ \_ operazioni \_ DS** Error Error.</span><span class="sxs-lookup"><span data-stu-id="74dd6-113">In the example, 8224L corresponds to the error **ERROR\_DS\_OPERATIONS\_ERROR**.</span></span>
4.  <span data-ttu-id="74dd6-114">Sostituire l'errore di prefisso **\_ DS** con **LDAP \_**.</span><span class="sxs-lookup"><span data-stu-id="74dd6-114">Replace the prefix **ERROR\_DS** with **LDAP\_**.</span></span> <span data-ttu-id="74dd6-115">Nell'esempio, la nuova definizione è un **\_ \_ errore di operazioni LDAP**.</span><span class="sxs-lookup"><span data-stu-id="74dd6-115">In the example, the new definition is **LDAP\_OPERATIONS\_ERROR**.</span></span>
5.  <span data-ttu-id="74dd6-116">Cercare nel file Winldap. h il valore della definizione di errore LDAP.</span><span class="sxs-lookup"><span data-stu-id="74dd6-116">Search in the Winldap.h file for the value of the LDAP error definition.</span></span> <span data-ttu-id="74dd6-117">Nell'esempio, il valore dell' **errore di \_ operazioni \_ LDAP** nel file Winldap. h è 0x01.</span><span class="sxs-lookup"><span data-stu-id="74dd6-117">In the example, the value of **LDAP\_OPERATIONS\_ERROR** in the Winldap.h file is 0x01.</span></span>

 

 




