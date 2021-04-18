---
description: La proprietà ProductCode è un identificatore univoco per la versione specifica del prodotto, rappresentata come GUID di stringa, ad esempio &\# 0034; {12345678-1234-1234-1234-123456789012}&\# 0034;.
ms.assetid: 33cedd37-0343-471c-ad4b-0db5f98d5894
title: Proprietà ProductCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a714687ab49bca07d1137b3395cb19ddba0944
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330620"
---
# <a name="productcode-property"></a>Proprietà ProductCode

La proprietà **ProductCode** è un identificatore univoco per la versione specifica del prodotto, rappresentata come [GUID](guid.md)di stringa, ad esempio " {12345678-1234-1234-1234-123456789012} ". Le lettere usate in questo GUID devono essere maiuscole. Questo ID deve variare per versioni e linguaggi diversi.

Un aggiornamento del prodotto che aggiorna un prodotto in un prodotto completamente nuovo deve modificare anche il codice del prodotto. Alle versioni a 32 bit e a 64 bit del pacchetto di un'applicazione devono essere assegnati codici di prodotto diversi.

**ProductCode** viene annunciato come una proprietà del prodotto ed è il metodo principale per specificare il prodotto. Questa proprietà è obbligatoria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




