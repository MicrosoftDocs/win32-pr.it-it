---
description: 'I valori del registro di sistema di WFP si trovano nella seguente chiave del registro di sistema: HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon.'
ms.assetid: d4da7f24-1e5d-4ea2-98e8-049e7eaefae1
title: Valori del registro di sistema WFP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb8db23800ebbead68f34eaf0fa9fffd772f01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317621"
---
# <a name="wfp-registry-values"></a>Valori del registro di sistema WFP

\[I valori del registro di sistema WFP non sono supportati a partire da Windows Vista.\]

WFP utilizza diversi valori del registro di sistema per le impostazioni di personalizzazione. I valori del registro di sistema di WFP si trovano nella seguente chiave del registro di sistema:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
```

Di seguito sono riportati i valori del registro di sistema di WFP.

<dl> <dt>

<span id="SFCDllCacheDir"></span><span id="sfcdllcachedir"></span><span id="SFCDLLCACHEDIR"></span>**SFCDllCacheDir**
</dt> <dd>

Percorso della cache. Deve trattarsi di un percorso locale. Il valore predefinito è% SystemRoot% \\ system32 \\ dllcache.

</dd> <dt>

<span id="SFCQuota"></span><span id="sfcquota"></span><span id="SFCQUOTA"></span>**SFCQuota**
</dt> <dd>

Opzioni di quota. Il valore del registro di sistema può essere uno dei valori seguenti.



| Valore                  | Significato                                                  |
|------------------------|----------------------------------------------------------|
| SFC \_ quota \_ tutti \_ i file | Le dimensioni della cache DLL sono illimitate. Questo è il valore predefinito. |
| Altri valori           | Dimensione della cache DLL, in file.                         |



 

</dd> <dt>

<span id="SFCScan"></span><span id="sfcscan"></span><span id="SFCSCAN"></span>**SFCScan**
</dt> <dd>

Opzioni di analisi. Il valore del registro di sistema può essere uno dei valori seguenti.



| Valore             | Significato                                                   |
|-------------------|-----------------------------------------------------------|
| Analisi SFC- \_ \_ normale | Non eseguire l'analisi dei file protetti all'avvio. Questo è il valore predefinito. |
| \_Analisi SFC \_ sempre | Analizza i file protetti a ogni avvio.                       |
| \_Analisi SFC \_ una volta   | Analizza i file protetti all'avvio successivo.                    |



 

</dd> </dl>

 

 



