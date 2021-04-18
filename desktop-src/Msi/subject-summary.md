---
description: Il valore della proprietà riepilogo oggetto comunica il nome del prodotto, della trasformazione o della patch installata dal pacchetto.
ms.assetid: fb08a240-db30-477f-8dc0-701156d73cfc
title: Proprietà di riepilogo oggetto
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d21139f686bc8a6cfc5ba2edecdfc57c349d84ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327312"
---
# <a name="subject-summary-property"></a>Proprietà di riepilogo oggetto

Il valore della proprietà **Riepilogo oggetto** comunica il nome del prodotto, della trasformazione o della patch installata dal pacchetto.

Per fornire il valore di questa proprietà nelle informazioni di riepilogo, spetta all'autore di un database di installazione, di una trasformazione o di un pacchetto di patch. Per determinare il valore corretto, gli autori devono eseguire le operazioni seguenti.

-   Impostare la proprietà **Summary del soggetto** in un pacchetto di installazione sullo stesso valore della proprietà [**ProductName**](productname.md) .
-   Impostare la proprietà **Riepilogo oggetto** in una trasformazione sullo stesso valore della proprietà **Riepilogo oggetto** nel pacchetto di installazione originale.
-   Impostare la proprietà **Riepilogo oggetto** nelle informazioni di riepilogo di un pacchetto di patch su una breve descrizione della patch che include il nome del prodotto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md)
</dt> <dt>

[Descrizioni delle proprietà di riepilogo](summary-property-descriptions.md)
</dt> </dl>

 

 




