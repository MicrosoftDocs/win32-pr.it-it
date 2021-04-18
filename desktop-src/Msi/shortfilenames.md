---
description: L'impostazione della proprietà SHORTFILENAMES causa l'utilizzo di nomi di file brevi per i nomi dei file di destinazione, anziché nomi di file lunghi. Non influisce sui nomi di file che il programma di installazione cerca nell'origine.
ms.assetid: b330f9c3-3297-45cf-915c-5fbb291b8afb
title: Proprietà SHORTFILENAMES
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e347e5ec400a1593858f0cac558f33528e25396e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333669"
---
# <a name="shortfilenames-property"></a>Proprietà SHORTFILENAMES

L'impostazione della proprietà **SHORTFILENAMES** causa l'utilizzo di nomi di file brevi per i nomi dei file di destinazione, anziché nomi di file lunghi. Non influisce sui nomi di file che il programma di installazione cerca nell'origine.

## <a name="default-value"></a>Valore predefinito

I nomi lunghi vengono usati dal programma di installazione se la proprietà **SHORTFILENAMES** non è impostata e il volume di destinazione supporta nomi lunghi. I nomi brevi vengono usati dal programma di installazione se il volume di destinazione non supporta nomi lunghi.

## <a name="remarks"></a>Commenti

Quando viene impostata la proprietà **SHORTFILENAMES** , il programma di installazione crea le cartelle e installa i file usando nomi di file brevi da qualsiasi coppia di brevi \| lunghezza elencata nella [tabella file](file-table.md) o nella [tabella di directory](directory-table.md).

Le applicazioni possono utilizzare la funzione [**GetShortPathName**](/windows/win32/api/fileapi/nf-fileapi-getshortpathnamew) per recuperare il formato di percorso breve di un percorso di file specificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 
