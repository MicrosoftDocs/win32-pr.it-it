---
title: Mapping della sintassi di Active Directory alla sintassi ADSI
description: Nella tabella seguente viene eseguito il mapping della sintassi Active Directory alle relative sintassi ADSI.
ms.assetid: ffb40eff-e137-4d6a-81e7-24d2cbbdbfbf
ms.tgt_platform: multiple
keywords:
- attributi ADSI, mapping Active Directory sintassi alla sintassi ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ba332a39a5d2452925f1a8f1cc8c8ca766ca10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297667"
---
# <a name="mapping-active-directory-syntax-to-adsi-syntax"></a><span data-ttu-id="4d9ae-104">Mapping della sintassi di Active Directory alla sintassi ADSI</span><span class="sxs-lookup"><span data-stu-id="4d9ae-104">Mapping Active Directory Syntax to ADSI Syntax</span></span>

<span data-ttu-id="4d9ae-105">Nella tabella seguente viene eseguito il mapping della sintassi Active Directory alle relative sintassi ADSI.</span><span class="sxs-lookup"><span data-stu-id="4d9ae-105">The following table maps the Active Directory syntaxes to their corresponding ADSI syntaxes.</span></span>



| <span data-ttu-id="4d9ae-106">ID sintassi attributo</span><span class="sxs-lookup"><span data-stu-id="4d9ae-106">Attribute syntax ID</span></span> | <span data-ttu-id="4d9ae-107">Tipo di sintassi Active Directory</span><span class="sxs-lookup"><span data-stu-id="4d9ae-107">Active Directory syntax type</span></span>             | <span data-ttu-id="4d9ae-108">Tipo di sintassi ADSI equivalente</span><span class="sxs-lookup"><span data-stu-id="4d9ae-108">Equivalent ADSI syntax type</span></span>                                         |
|---------------------|------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="4d9ae-109">2.5.5.1</span><span class="sxs-lookup"><span data-stu-id="4d9ae-109">2.5.5.1</span></span><br/>  | <span data-ttu-id="4d9ae-110">Stringa DN</span><span class="sxs-lookup"><span data-stu-id="4d9ae-110">DN String</span></span><br/>                     | <span data-ttu-id="4d9ae-111">Stringa DN</span><span class="sxs-lookup"><span data-stu-id="4d9ae-111">DN String</span></span><br/>                                                |
| <span data-ttu-id="4d9ae-112">2.5.5.2</span><span class="sxs-lookup"><span data-stu-id="4d9ae-112">2.5.5.2</span></span><br/>  | <span data-ttu-id="4d9ae-113">ID dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4d9ae-113">Object ID</span></span><br/>                     | <span data-ttu-id="4d9ae-114">Stringa CaseIgnore</span><span class="sxs-lookup"><span data-stu-id="4d9ae-114">CaseIgnore String</span></span><br/>                                        |
| <span data-ttu-id="4d9ae-115">2.5.5.3</span><span class="sxs-lookup"><span data-stu-id="4d9ae-115">2.5.5.3</span></span><br/>  | <span data-ttu-id="4d9ae-116">Stringa distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="4d9ae-116">Case Sensitive String</span></span><br/>         | <span data-ttu-id="4d9ae-117">Stringa CaseExact</span><span class="sxs-lookup"><span data-stu-id="4d9ae-117">CaseExact String</span></span><br/>                                         |
| <span data-ttu-id="4d9ae-118">2.5.5.4</span><span class="sxs-lookup"><span data-stu-id="4d9ae-118">2.5.5.4</span></span><br/>  | <span data-ttu-id="4d9ae-119">Stringa case ignorata</span><span class="sxs-lookup"><span data-stu-id="4d9ae-119">Case Ignored String</span></span><br/>           | <span data-ttu-id="4d9ae-120">Stringa CaseIgnore</span><span class="sxs-lookup"><span data-stu-id="4d9ae-120">CaseIgnore String</span></span><br/>                                        |
| <span data-ttu-id="4d9ae-121">2.5.5.5</span><span class="sxs-lookup"><span data-stu-id="4d9ae-121">2.5.5.5</span></span><br/>  | <span data-ttu-id="4d9ae-122">Stringa del case di stampa</span><span class="sxs-lookup"><span data-stu-id="4d9ae-122">Print Case String</span></span><br/>             | <span data-ttu-id="4d9ae-123">Stringa stampabile</span><span class="sxs-lookup"><span data-stu-id="4d9ae-123">Printable String</span></span><br/>                                         |
| <span data-ttu-id="4d9ae-124">2.5.5.6</span><span class="sxs-lookup"><span data-stu-id="4d9ae-124">2.5.5.6</span></span><br/>  | <span data-ttu-id="4d9ae-125">Stringa numerica</span><span class="sxs-lookup"><span data-stu-id="4d9ae-125">Numeric String</span></span><br/>                | <span data-ttu-id="4d9ae-126">Stringa numerica</span><span class="sxs-lookup"><span data-stu-id="4d9ae-126">Numeric String</span></span><br/>                                           |
| <span data-ttu-id="4d9ae-127">2.5.5.7</span><span class="sxs-lookup"><span data-stu-id="4d9ae-127">2.5.5.7</span></span><br/>  | <span data-ttu-id="4d9ae-128">**O** Nome DNWithOctetString</span><span class="sxs-lookup"><span data-stu-id="4d9ae-128">**OR** Name DNWithOctetString</span></span><br/> | <span data-ttu-id="4d9ae-129">Non supportato</span><span class="sxs-lookup"><span data-stu-id="4d9ae-129">Not Supported</span></span><br/>                                            |
| <span data-ttu-id="4d9ae-130">2.5.5.8</span><span class="sxs-lookup"><span data-stu-id="4d9ae-130">2.5.5.8</span></span><br/>  | <span data-ttu-id="4d9ae-131">Boolean</span><span class="sxs-lookup"><span data-stu-id="4d9ae-131">Boolean</span></span><br/>                       | <span data-ttu-id="4d9ae-132">Boolean</span><span class="sxs-lookup"><span data-stu-id="4d9ae-132">Boolean</span></span><br/>                                                  |
| <span data-ttu-id="4d9ae-133">2.5.5.9</span><span class="sxs-lookup"><span data-stu-id="4d9ae-133">2.5.5.9</span></span><br/>  | <span data-ttu-id="4d9ae-134">Integer</span><span class="sxs-lookup"><span data-stu-id="4d9ae-134">Integer</span></span><br/>                       | <span data-ttu-id="4d9ae-135">Integer</span><span class="sxs-lookup"><span data-stu-id="4d9ae-135">Integer</span></span><br/>                                                  |
| <span data-ttu-id="4d9ae-136">2.5.5.10</span><span class="sxs-lookup"><span data-stu-id="4d9ae-136">2.5.5.10</span></span><br/> | <span data-ttu-id="4d9ae-137">Stringa ottetto</span><span class="sxs-lookup"><span data-stu-id="4d9ae-137">Octet String</span></span><br/>                  | <span data-ttu-id="4d9ae-138">Stringa ottetto</span><span class="sxs-lookup"><span data-stu-id="4d9ae-138">Octet String</span></span><br/>                                             |
| <span data-ttu-id="4d9ae-139">2.5.5.11</span><span class="sxs-lookup"><span data-stu-id="4d9ae-139">2.5.5.11</span></span><br/> | <span data-ttu-id="4d9ae-140">Tempo</span><span class="sxs-lookup"><span data-stu-id="4d9ae-140">Time</span></span><br/>                          | <span data-ttu-id="4d9ae-141">Ora UTC</span><span class="sxs-lookup"><span data-stu-id="4d9ae-141">UTC Time</span></span><br/>                                                 |
| <span data-ttu-id="4d9ae-142">2.5.5.12</span><span class="sxs-lookup"><span data-stu-id="4d9ae-142">2.5.5.12</span></span><br/> | <span data-ttu-id="4d9ae-143">Unicode</span><span class="sxs-lookup"><span data-stu-id="4d9ae-143">Unicode</span></span><br/>                       | <span data-ttu-id="4d9ae-144">Stringa Case Ignore</span><span class="sxs-lookup"><span data-stu-id="4d9ae-144">Case Ignore String</span></span><br/>                                       |
| <span data-ttu-id="4d9ae-145">2.5.5.13</span><span class="sxs-lookup"><span data-stu-id="4d9ae-145">2.5.5.13</span></span><br/> | <span data-ttu-id="4d9ae-146">Indirizzo</span><span class="sxs-lookup"><span data-stu-id="4d9ae-146">Address</span></span><br/>                       | <span data-ttu-id="4d9ae-147">Non supportato</span><span class="sxs-lookup"><span data-stu-id="4d9ae-147">Not Supported</span></span><br/>                                            |
| <span data-ttu-id="4d9ae-148">2.5.5.14</span><span class="sxs-lookup"><span data-stu-id="4d9ae-148">2.5.5.14</span></span><br/> | <span data-ttu-id="4d9ae-149">Distname-Address</span><span class="sxs-lookup"><span data-stu-id="4d9ae-149">Distname-Address</span></span><br/>              |                                                                     |
| <span data-ttu-id="4d9ae-150">2.5.5.15</span><span class="sxs-lookup"><span data-stu-id="4d9ae-150">2.5.5.15</span></span><br/> | <span data-ttu-id="4d9ae-151">Descrittore di sicurezza NT</span><span class="sxs-lookup"><span data-stu-id="4d9ae-151">NT Security Descriptor</span></span><br/>        | [<span data-ttu-id="4d9ae-152">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="4d9ae-152">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)<br/> |
| <span data-ttu-id="4d9ae-153">2.5.5.16</span><span class="sxs-lookup"><span data-stu-id="4d9ae-153">2.5.5.16</span></span><br/> | <span data-ttu-id="4d9ae-154">Integer grande</span><span class="sxs-lookup"><span data-stu-id="4d9ae-154">Large Integer</span></span><br/>                 | [<span data-ttu-id="4d9ae-155">**IADsLargeInteger**</span><span class="sxs-lookup"><span data-stu-id="4d9ae-155">**IADsLargeInteger**</span></span>](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)<br/>             |
| <span data-ttu-id="4d9ae-156">2.5.5.17</span><span class="sxs-lookup"><span data-stu-id="4d9ae-156">2.5.5.17</span></span><br/> | <span data-ttu-id="4d9ae-157">SID</span><span class="sxs-lookup"><span data-stu-id="4d9ae-157">SID</span></span><br/>                           | <span data-ttu-id="4d9ae-158">Stringa ottetto</span><span class="sxs-lookup"><span data-stu-id="4d9ae-158">Octet String</span></span><br/>                                             |



 

 

 





