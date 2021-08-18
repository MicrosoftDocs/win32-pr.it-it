---
description: L'impostazione della proprietà SHORTFILENAMES comporta l'utilizzo di nomi di file brevi per i nomi dei file di destinazione, anziché per nomi di file lunghi. Non influisce sui nomi di file cercati dal programma di installazione nell'origine.
ms.assetid: b330f9c3-3297-45cf-915c-5fbb291b8afb
title: SHORTFILENAMES - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb64d9f2078a1455aa79bfec077e6108f4a8a5bd9ced7d246c5fe588919b33d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628411"
---
# <a name="shortfilenames-property"></a>SHORTFILENAMES - proprietà

**L'impostazione della proprietà SHORTFILENAMES** comporta l'utilizzo di nomi di file brevi per i nomi dei file di destinazione, anziché per nomi di file lunghi. Non influisce sui nomi di file cercati dal programma di installazione nell'origine.

## <a name="default-value"></a>Valore predefinito

I nomi lunghi vengono usati dal programma di installazione se la **proprietà SHORTFILENAMES** non è impostata e il volume di destinazione supporta i nomi lunghi. I nomi brevi vengono usati dal programma di installazione se il volume di destinazione non supporta i nomi lunghi.

## <a name="remarks"></a>Commenti

Quando la **proprietà SHORTFILENAMES** è impostata, il programma di installazione crea cartelle e installa i file usando nomi di file brevi di qualsiasi coppia breve lunga elencata nella tabella File o \| [directory](directory-table.md). [](file-table.md)

Le applicazioni possono usare [**la funzione GetShortPathName**](/windows/win32/api/fileapi/nf-fileapi-getshortpathnamew) per recuperare il formato di percorso breve di un percorso di file specificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Per informazioni [Windows service](windows-installer-portal.md) pack minimo necessario per Run-Time versione del programma di installazione di Windows, vedere i requisiti minimi Windows Service Pack.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 
