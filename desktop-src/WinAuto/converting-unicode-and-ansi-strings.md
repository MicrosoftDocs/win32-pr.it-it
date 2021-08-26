---
title: Conversione di stringhe Unicode e ANSI
description: Microsoft Active Accessibility usa stringhe Unicode come definito dal tipo di dati BSTR.
ms.assetid: 47f525fe-6d18-43b9-a706-e49afa796830
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b001791b2de2bde4c1efa0b09dcee55203a6cf69a41d5b7927c5df5438de90fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030941"
---
# <a name="converting-unicode-and-ansi-strings"></a>Conversione di stringhe Unicode e ANSI

Microsoft Active Accessibility usa stringhe Unicode come definito dal **tipo di dati BSTR.** Se l'applicazione non usa stringhe Unicode o se si vogliono convertire stringhe per determinate chiamate API, usare le funzioni [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) Microsoft Win32 per eseguire la conversione necessaria.

Usare [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) per convertire una stringa Unicode in una stringa ANSI. La [**funzione MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) converte una stringa ANSI in una stringa Unicode.

Usare [**SysAllocString e**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) [**SysFreeString per**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) allocare e liberare tipi di dati **BSTR.**

Per altre informazioni su queste funzioni stringa, vedere i relativi riferimenti in Windows Software Development Kit (SDK).

 

 