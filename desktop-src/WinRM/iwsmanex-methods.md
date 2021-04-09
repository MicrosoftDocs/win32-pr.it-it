---
title: Metodi IWSManEx
description: L'interfaccia IWSManEx espone i metodi seguenti.
ms.assetid: 609F5D75-879A-4681-B746-8C7A8757F062
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa7279d15d98b3e534e57a83813cd9cbe75a09fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104043996"
---
# <a name="iwsmanex-methods"></a><span data-ttu-id="cd54b-103">Metodi IWSManEx</span><span class="sxs-lookup"><span data-stu-id="cd54b-103">IWSManEx Methods</span></span>

<span data-ttu-id="cd54b-104">L'interfaccia [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) espone i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="cd54b-104">The [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cd54b-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="cd54b-105">In this section</span></span>

-   [<span data-ttu-id="cd54b-106">**Metodo CreateResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="cd54b-106">**CreateResourceLocator Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator)
-   [<span data-ttu-id="cd54b-107">**Metodo EnumerationFlagHierarchyDeep**</span><span class="sxs-lookup"><span data-stu-id="cd54b-107">**EnumerationFlagHierarchyDeep Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep)
-   [<span data-ttu-id="cd54b-108">**Metodo EnumerationFlagHierarchyDeepBasePropsOnly**</span><span class="sxs-lookup"><span data-stu-id="cd54b-108">**EnumerationFlagHierarchyDeepBasePropsOnly Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly)
-   [<span data-ttu-id="cd54b-109">**Metodo EnumerationFlagHierarchyShallow**</span><span class="sxs-lookup"><span data-stu-id="cd54b-109">**EnumerationFlagHierarchyShallow Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow)
-   [<span data-ttu-id="cd54b-110">**Metodo EnumerationFlagNonXmlText**</span><span class="sxs-lookup"><span data-stu-id="cd54b-110">**EnumerationFlagNonXmlText Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext)
-   [<span data-ttu-id="cd54b-111">**Metodo EnumerationFlagReturnEPR**</span><span class="sxs-lookup"><span data-stu-id="cd54b-111">**EnumerationFlagReturnEPR Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr)
-   [<span data-ttu-id="cd54b-112">**Metodo EnumerationFlagReturnObject**</span><span class="sxs-lookup"><span data-stu-id="cd54b-112">**EnumerationFlagReturnObject Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject)
-   [<span data-ttu-id="cd54b-113">**Metodo EnumerationFlagReturnObjectAndEPR**</span><span class="sxs-lookup"><span data-stu-id="cd54b-113">**EnumerationFlagReturnObjectAndEPR Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr)
-   [<span data-ttu-id="cd54b-114">**Metodo GetErrorMessage**</span><span class="sxs-lookup"><span data-stu-id="cd54b-114">**GetErrorMessage Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage)
-   [<span data-ttu-id="cd54b-115">**Metodo SessionFlagCredUsernamePassword**</span><span class="sxs-lookup"><span data-stu-id="cd54b-115">**SessionFlagCredUsernamePassword Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagcredusernamepassword)
-   [<span data-ttu-id="cd54b-116">**Metodo SessionFlagEnableSPNServerPort**</span><span class="sxs-lookup"><span data-stu-id="cd54b-116">**SessionFlagEnableSPNServerPort Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagenablespnserverport)
-   [<span data-ttu-id="cd54b-117">**Metodo SessionFlagNoEncryption**</span><span class="sxs-lookup"><span data-stu-id="cd54b-117">**SessionFlagNoEncryption Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption)
-   [<span data-ttu-id="cd54b-118">**Metodo SessionFlagSkipCACheck**</span><span class="sxs-lookup"><span data-stu-id="cd54b-118">**SessionFlagSkipCACheck Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcacheck)
-   [<span data-ttu-id="cd54b-119">**Metodo SessionFlagSkipCNCheck**</span><span class="sxs-lookup"><span data-stu-id="cd54b-119">**SessionFlagSkipCNCheck Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcncheck)
-   [<span data-ttu-id="cd54b-120">**Metodo SessionFlagUseBasic**</span><span class="sxs-lookup"><span data-stu-id="cd54b-120">**SessionFlagUseBasic Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusebasic)
-   [<span data-ttu-id="cd54b-121">**Metodo SessionFlagUseDigest**</span><span class="sxs-lookup"><span data-stu-id="cd54b-121">**SessionFlagUseDigest Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusedigest)
-   [<span data-ttu-id="cd54b-122">**Metodo SessionFlagUseKerberos**</span><span class="sxs-lookup"><span data-stu-id="cd54b-122">**SessionFlagUseKerberos Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusekerberos)
-   [<span data-ttu-id="cd54b-123">**Metodo SessionFlagUseNegotiate**</span><span class="sxs-lookup"><span data-stu-id="cd54b-123">**SessionFlagUseNegotiate Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenegotiate)
-   [<span data-ttu-id="cd54b-124">**Metodo SessionFlagUseNoAuthentication**</span><span class="sxs-lookup"><span data-stu-id="cd54b-124">**SessionFlagUseNoAuthentication Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenoauthentication)
-   [<span data-ttu-id="cd54b-125">**Metodo SessionFlagUTF8**</span><span class="sxs-lookup"><span data-stu-id="cd54b-125">**SessionFlagUTF8 Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagutf8)

 

 




