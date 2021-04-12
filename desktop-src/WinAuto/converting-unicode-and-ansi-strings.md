---
title: Conversione di stringhe Unicode e ANSI
description: Microsoft Active Accessibility utilizza stringhe Unicode come definito dal tipo di dati BSTR.
ms.assetid: 47f525fe-6d18-43b9-a706-e49afa796830
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fa26813c61be0a3959593f370016cfce0211ea9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338342"
---
# <a name="converting-unicode-and-ansi-strings"></a><span data-ttu-id="0d753-103">Conversione di stringhe Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="0d753-103">Converting Unicode and ANSI Strings</span></span>

<span data-ttu-id="0d753-104">Microsoft Active Accessibility utilizza stringhe Unicode come definito dal tipo di dati **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="0d753-104">Microsoft Active Accessibility uses Unicode strings as defined by the **BSTR** data type.</span></span> <span data-ttu-id="0d753-105">Se l'applicazione non utilizza stringhe Unicode o se si desidera convertire le stringhe per determinate chiamate API, utilizzare le funzioni Microsoft Win32 [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) per eseguire la conversione necessaria.</span><span class="sxs-lookup"><span data-stu-id="0d753-105">If your application does not use Unicode strings, or if you want to convert strings for certain API calls, use the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) and [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) Microsoft Win32 functions to perform the necessary conversion.</span></span>

<span data-ttu-id="0d753-106">Usare [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) per convertire una stringa Unicode in una stringa ANSI.</span><span class="sxs-lookup"><span data-stu-id="0d753-106">Use [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) to convert a Unicode string to an ANSI string.</span></span> <span data-ttu-id="0d753-107">La funzione [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) converte una stringa ANSI in una stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="0d753-107">The [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function converts an ANSI string to a Unicode string.</span></span>

<span data-ttu-id="0d753-108">Usare [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) e [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) per allocare e liberare i tipi di dati **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="0d753-108">Use [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) and [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) to allocate and free **BSTR** data types.</span></span>

<span data-ttu-id="0d753-109">Per ulteriori informazioni su queste funzioni per i valori stringa, vedere i relativi riferimenti in Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="0d753-109">For more information about these string functions, see their references in the Windows Software Development Kit (SDK).</span></span>

 

 