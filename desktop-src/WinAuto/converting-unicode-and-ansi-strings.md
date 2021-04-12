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
# <a name="converting-unicode-and-ansi-strings"></a>Conversione di stringhe Unicode e ANSI

Microsoft Active Accessibility utilizza stringhe Unicode come definito dal tipo di dati **BSTR** . Se l'applicazione non utilizza stringhe Unicode o se si desidera convertire le stringhe per determinate chiamate API, utilizzare le funzioni Microsoft Win32 [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) per eseguire la conversione necessaria.

Usare [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) per convertire una stringa Unicode in una stringa ANSI. La funzione [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) converte una stringa ANSI in una stringa Unicode.

Usare [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) e [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) per allocare e liberare i tipi di dati **BSTR** .

Per ulteriori informazioni su queste funzioni per i valori stringa, vedere i relativi riferimenti in Windows Software Development Kit (SDK).

 

 