---
description: La classe CHString espone i metodi seguenti.
ms.assetid: C064D6DE-14C4-4143-8164-B367C10CBF8E
ms.tgt_platform: multiple
title: Metodi di CHString
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50d15726702177aa484a070cca3ec1aab56d708b57991d3ff6a7aae43b1ccf68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556956"
---
# <a name="chstring-methods"></a>Metodi di CHString

\[La [**classe CHString**](chstring.md) fa parte del framework del provider WMI che è ora considerato in stato finale e non saranno disponibili altri aggiornamenti, miglioramenti o sviluppo per problemi non correlati alla sicurezza che interessano queste librerie. Le [API MI devono essere](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) usate per tutti i nuovi sviluppi.\]

La [**classe CHString**](chstring.md) espone i metodi seguenti.

## <a name="in-this-section"></a>Contenuto della sezione

-   [**Metodo AllocSysString**](/windows/desktop/api/ChString/nf-chstring-chstring-allocsysstring)
-   [**Costruttori CHString**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_))
-   [**Metodo Collate**](/windows/desktop/api/ChString/nf-chstring-chstring-collate)
-   [**Compare (metodo)**](/windows/desktop/api/ChString/nf-chstring-chstring-compare)
-   [**Metodo CompareNoCase**](/windows/desktop/api/ChString/nf-chstring-chstring-comparenocase)
-   [**Metodo empty**](/windows/desktop/api/ChString/nf-chstring-chstring-empty)
-   [**Trovare i metodi**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))
-   [**Metodo FindOneOf**](/windows/desktop/api/ChString/nf-chstring-chstring-findoneof)
-   [**Metodi di formattazione**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))
-   [**Metodi formatMessageW**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))
-   [**Metodo FormatV**](/windows/desktop/api/ChString/nf-chstring-chstring-formatv)
-   [**Metodo FreeExtra**](/windows/desktop/api/ChString/nf-chstring-chstring-freeextra)
-   [**Metodo GetAllocLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getalloclength)
-   [**Metodo GetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))
-   [**GetBuffer (metodo)**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer)
-   [**Metodo GetBufferSetLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffersetlength)
-   [**Metodo GetData**](/windows/desktop/api/ChString/nf-chstring-chstring-getdata)
-   [**Metodo GetLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getlength)
-   [**IsEmpty (metodo)**](/windows/desktop/api/ChString/nf-chstring-chstring-isempty)
-   [**Metodo Left**](/windows/desktop/api/ChString/nf-chstring-chstring-left)
-   [**Metodo LoadStringW**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))
-   [**Metodo LockBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-lockbuffer)
-   [**Metodo MakeLower**](/windows/desktop/api/ChString/nf-chstring-chstring-makelower)
-   [**Metodo MakeReverse**](/windows/desktop/api/ChString/nf-chstring-chstring-makereverse)
-   [**Metodo MakeUpper**](/windows/desktop/api/ChString/nf-chstring-chstring-makeupper)
-   [**Metodi mid**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))
-   [**Metodo \[ \] operatore**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))
-   [**CHString::operator+**](chstring--operator-plus.md)
-   [**CHString::operator+=**](chstring--operator-plus-equal.md)
-   [**CHString::operator=**](chstring--operator-equal.md)
-   [**Metodo operator==(constCHString&, constCHString&)**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))
-   [**Metodo operator==(constCHString&, constLPCWSTR&)**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))
-   [**metodo>(constCHString&, constCHString&)**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))
-   [**metodo>(constCHString&, constLPCWSTR&)**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))
-   [**metodo>operatore =(constCHString&, constCHString&)**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85))
-   [**metodo>operatore =(constCHString&, constLPCWSTR&)**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))
-   [**metodo<(constCHString&, constCHString&)**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))
-   [**metodo<(constCHString&, constLPCWSTR&)**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))
-   [**metodo<operatore =(constCHString&, constCHString&)**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))
-   [**metodo<operatore =(constCHString&, constLPCWSTR&)**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))
-   [**Metodo operator!=(constCHString&, constCHString&)**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))
-   [**Metodo operator!=(constCHString&, constLPCWSTR&)**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))
-   [**Metodo LPCWSTR dell'operatore**](/windows/desktop/api/ChString/nf-chstring-chstring-operatorlpcwstr)
-   [**Metodo ReleaseBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-releasebuffer)
-   [**Metodo ReverseFind**](/windows/desktop/api/ChString/nf-chstring-chstring-reversefind)
-   [**Metodo Right**](/windows/desktop/api/ChString/nf-chstring-chstring-right)
-   [**Metodo SetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-setat)
-   [**Metodo SpanExcluding**](/windows/desktop/api/ChString/nf-chstring-chstring-spanexcluding)
-   [**Metodo SpanIncluding**](/windows/desktop/api/ChString/nf-chstring-chstring-spanincluding)
-   [**Metodo TrimLeft**](/windows/desktop/api/ChString/nf-chstring-chstring-trimleft)
-   [**Metodo TrimRight**](/windows/desktop/api/ChString/nf-chstring-chstring-trimright)
-   [**Metodo UnlockBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-unlockbuffer)

 

 
