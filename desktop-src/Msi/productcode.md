---
description: La proprietà ProductCode è un identificatore univoco per la versione specifica del prodotto, rappresentato come GUID di stringa, ad esempio &\# 0034; {12345678-1234-1234-1234-123456789012}&\# 0034;.
ms.assetid: 33cedd37-0343-471c-ad4b-0db5f98d5894
title: ProductCode - proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a77ba270075b214d5eee2ee804c6849a2ef71561610ee60ae3eb4941e43465c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753911"
---
# <a name="productcode-property"></a>ProductCode - proprietà

La **proprietà ProductCode** è un identificatore univoco per la versione specifica del prodotto, rappresentato come [GUID](guid.md)di stringa, ad esempio " {12345678-1234-1234-1234-123456789012} ". Le lettere usate in questo GUID devono essere maiuscole. Questo ID deve variare per versioni e lingue diverse.

Anche un aggiornamento del prodotto che aggiorna un prodotto in un prodotto completamente nuovo deve modificare il codice del prodotto. Alle versioni a 32 bit e a 64 bit del pacchetto di un'applicazione devono essere assegnati codici prodotto diversi.

ProductCode **viene** annunciato come proprietà del prodotto ed è il metodo principale per specificare il prodotto. Questa proprietà è REQUIRED.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




