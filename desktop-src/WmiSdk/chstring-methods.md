---
description: La classe CHString espone i metodi seguenti.
ms.assetid: C064D6DE-14C4-4143-8164-B367C10CBF8E
ms.tgt_platform: multiple
title: Metodi CHString
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e15a26bf2b5945990f8cd37ee67c2953395ca98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050232"
---
# <a name="chstring-methods"></a>Metodi CHString

\[La classe [**CHString**](chstring.md) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie. Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]

La classe [**CHString**](chstring.md) espone i metodi seguenti.

## <a name="in-this-section"></a>Contenuto della sezione

-   [**Metodo AllocSysString**](/windows/desktop/api/ChString/nf-chstring-chstring-allocsysstring)
-   [**Costruttori CHString**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_))
-   [**Metodo COLLATE**](/windows/desktop/api/ChString/nf-chstring-chstring-collate)
-   [**Compare (metodo)**](/windows/desktop/api/ChString/nf-chstring-chstring-compare)
-   [**Metodo CompareNoCase**](/windows/desktop/api/ChString/nf-chstring-chstring-comparenocase)
-   [**Metodo Empty**](/windows/desktop/api/ChString/nf-chstring-chstring-empty)
-   [**Metodi Find**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))
-   [**Metodo FindOneOf**](/windows/desktop/api/ChString/nf-chstring-chstring-findoneof)
-   [**Metodi Format**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))
-   [**Metodi FormatMessageW**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))
-   [**Metodo FormatV**](/windows/desktop/api/ChString/nf-chstring-chstring-formatv)
-   [**Metodo FreeExtra**](/windows/desktop/api/ChString/nf-chstring-chstring-freeextra)
-   [**Metodo GetAllocLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getalloclength)
-   [**Metodo GetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))
-   [**GetBuffer (metodo)**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer)
-   [**Metodo GetBufferSetLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffersetlength)
-   [**GetData (metodo)**](/windows/desktop/api/ChString/nf-chstring-chstring-getdata)
-   [**Metodo GetLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getlength)
-   [**IsEmpty (metodo)**](/windows/desktop/api/ChString/nf-chstring-chstring-isempty)
-   [**Left (metodo)**](/windows/desktop/api/ChString/nf-chstring-chstring-left)
-   [**Metodo LoadStringW**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))
-   [**Metodo LockBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-lockbuffer)
-   [**Metodo MakeLower**](/windows/desktop/api/ChString/nf-chstring-chstring-makelower)
-   [**Metodo MakeReverse**](/windows/desktop/api/ChString/nf-chstring-chstring-makereverse)
-   [**Metodo MakeUpper**](/windows/desktop/api/ChString/nf-chstring-chstring-makeupper)
-   [**Metodi Mid**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))
-   [**operatore ( \[ \] metodo)**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))
-   [**CHString:: operator +**](chstring--operator-plus.md)
-   [**CHString:: operator + =**](chstring--operator-plus-equal.md)
-   [**CHString:: operator =**](chstring--operator-equal.md)
-   [**operator = = (constCHString&, constCHString&) (metodo)**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))
-   [**operator = = (constCHString&, constLPCWSTR&) (metodo)**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))
-   [**operatore> (constCHString&, constCHString&) (metodo)**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))
-   [**operatore> (constCHString&, constLPCWSTR&) (metodo)**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))
-   [**operatore>= (constCHString&, constCHString&) (metodo)**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85))
-   [**operatore>= (constCHString&, constLPCWSTR&) (metodo)**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))
-   [**operatore< (constCHString&, constCHString&) (metodo)**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))
-   [**operatore< (constCHString&, constLPCWSTR&) (metodo)**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))
-   [**operatore<= (constCHString&, constCHString&) (metodo)**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))
-   [**operatore<= (constCHString&, constLPCWSTR&) (metodo)**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))
-   [**operator! = (constCHString&, constCHString&) (metodo)**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))
-   [**operator! = (constCHString&, constLPCWSTR&) (metodo)**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))
-   [**operatore LPCWSTR (metodo)**](/windows/desktop/api/ChString/nf-chstring-chstring-operatorlpcwstr)
-   [**Metodo ReleaseBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-releasebuffer)
-   [**Metodo ReverseFind**](/windows/desktop/api/ChString/nf-chstring-chstring-reversefind)
-   [**Metodo Right**](/windows/desktop/api/ChString/nf-chstring-chstring-right)
-   [**Metodo SetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-setat)
-   [**Metodo SpanExcluding**](/windows/desktop/api/ChString/nf-chstring-chstring-spanexcluding)
-   [**Metodo SpanIncluding**](/windows/desktop/api/ChString/nf-chstring-chstring-spanincluding)
-   [**Metodo TrimLeft**](/windows/desktop/api/ChString/nf-chstring-chstring-trimleft)
-   [**Metodo TrimRight**](/windows/desktop/api/ChString/nf-chstring-chstring-trimright)
-   [**Metodo UnlockBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-unlockbuffer)

 

 
