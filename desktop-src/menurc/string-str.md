---
title: Struttura di stringhe
description: Rappresenta l'organizzazione dei dati in una risorsa della versione del file. Contiene una stringa che descrive un aspetto specifico di un file, ad esempio la versione di un file, le informazioni sul copyright o i marchi.
ms.assetid: fcc5ac68-4aec-4a3b-aa92-96fc50cc4ca2
keywords:
- Menu struttura di stringhe e altre risorse
topic_type:
- apiref
api_name:
- String
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a6db2c10e981ae059a46e84e7abfc4d6dfc372fc3c75c76cfc20fd8a8f42735d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776731"
---
# <a name="string-structure"></a>Struttura di stringhe

Rappresenta l'organizzazione dei dati in una risorsa della versione del file. Contiene una stringa che descrive un aspetto specifico di un file, ad esempio la versione di un file, le informazioni sul copyright o i marchi.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  WORD  Value;
} String;
```



## <a name="members"></a>Members

<dl> <dt>

**wLength**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Lunghezza, in byte, di questa **struttura** String.

</dd> <dt>

**wValueLength**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Dimensione, in parole, del **membro** Value.

</dd> <dt>

**wType**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Tipo di dati nella risorsa della versione. Questo membro è 1 se la risorsa versione contiene dati di testo e 0 se la risorsa versione contiene dati binari.

</dd> <dt>

**szKey**
</dt> <dd>

Tipo: **WCHAR**

</dd> <dd>

Stringa Unicode arbitraria. Il **membro szKey** può essere uno o più dei valori seguenti. Questi valori sono solo linee guida.

<dt>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>**Commenti**


</dt> <dd>

Il **membro Value** contiene eventuali informazioni aggiuntive che devono essere visualizzate a scopo diagnostico. Questa stringa può avere una lunghezza arbitraria.

</dd> <dt>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>**Companyname**


</dt> <dd>

Il **membro Value** identifica la società che ha prodotto il file. Ad esempio, "Microsoft Corporation" o "Standard Microsystems Corporation, Inc."

</dd> <dt>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>**FileDescription**


</dt> <dd>

Il **membro Value** descrive il file in modo che possa essere presentato agli utenti. Questa stringa può essere visualizzata in una casella di riepilogo quando l'utente sceglie i file da installare. Ad esempio, "Driver tastiera per tastiere di tipo AT" o "Microsoft Word per Windows".

</dd> <dt>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>**FileVersion**


</dt> <dd>

Il **membro Value** identifica la versione di questo file. Ad esempio, **Il** valore potrebbe essere "3,00A" o "5.00.RC2".

</dd> <dt>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>**InternalName**


</dt> <dd>

Il **membro Value** identifica il nome interno del file, se presente. Ad esempio, questa stringa può contenere il nome del modulo per una DLL, un nome di dispositivo virtuale per un dispositivo virtuale Windows o un nome di dispositivo per un driver di dispositivo MS-DOS.

</dd> <dt>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>**LegalCopyright**


</dt> <dd>

Il **membro Value** descrive tutte le comunicazioni sul copyright, i marchi e i marchi registrati che si applicano al file. Deve includere il testo completo di tutte le comunicazioni, i simboli legali, le date di copyright, i numeri dei marchi e così via. In inglese, questa stringa deve essere nel formato "Copyright Microsoft Corp. 1990 1994".

</dd> <dt>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>**Note legali**


</dt> <dd>

Il **membro Value** descrive tutti i marchi registrati e i marchi registrati che si applicano al file. Deve includere il testo completo di tutte le comunicazioni, i simboli legali, i numeri dei marchi e così via. In inglese questa stringa dovrebbe essere "Windows is a trademark of Microsoft Corporation".

</dd> <dt>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>**OriginalFilename**


</dt> <dd>

Il **membro Value** identifica il nome originale del file, senza includere un percorso. Ciò consente a un'applicazione di determinare se un file è stato rinominato da un utente. Questo nome potrebbe non essere in formato MS-DOS 8.3 se il file è specifico di un file non FAT file system.

</dd> <dt>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>**PrivateBuild**


</dt> <dd>

Il **membro Value** descrive da chi, dove e perché è stata compilata questa versione privata del file. Questa stringa deve essere presente solo se il flag **\_ VS FF \_ PRIVATEBUILD** è impostato nel membro **dwFileFlags** della [**struttura \_ FIXEDFILEINFO di VS.**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) Ad esempio, **Il valore** potrebbe essere "Compilato da UNANID2". \\

</dd> <dt>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>**Productname**


</dt> <dd>

Il **membro Value** identifica il nome del prodotto con cui viene distribuito il file. Ad esempio, questa stringa potrebbe essere "Microsoft Windows".

</dd> <dt>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>**Productversion**


</dt> <dd>

Il **membro Value** identifica la versione del prodotto con cui viene distribuito il file. Ad esempio, **Il** valore potrebbe essere "3,00A" o "5.00.RC2".

</dd> <dt>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>**SpecialBuild**


</dt> <dd>

Il **membro Value** descrive le differenze tra questa versione del file e la versione normale. Questa voce deve essere presente solo se il flag **\_ \_ SPECIALBUILD** di VS FF è impostato nel membro **dwFileFlags** della [**struttura \_ FIXEDFILEINFO di VS.**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) Ad esempio, **Il valore** potrebbe essere "Compilazione privata per La risoluzione di problemi del mouse in computer M250 e M250E".

</dd> </dl> </dd> <dt>

**Riempimento**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Il numero di zero parole necessario per allineare il **membro Value** su un limite a 32 bit.

</dd> <dt>

**Valore**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Stringa con terminazione zero. Per altre informazioni, vedere la descrizione del membro **szKey.**

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura non è una vera struttura in linguaggio C perché contiene membri a lunghezza variabile. Questa struttura è stata creata esclusivamente per rappresentare l'organizzazione dei dati in una risorsa versione e non viene visualizzata in nessuno dei file di intestazione forniti con Windows Software Development Kit (SDK).

Una **struttura String** può avere un valore **szKey,** ad esempio "CompanyName" e un **valore** "Microsoft Corporation". **Un'altra** struttura String con lo **stesso valore szKey** può **contenere un valore** "Microsoft GmbH". Questo problema può verificarsi se la seconda struttura **String** è stata associata a una struttura [**StringTable**](stringtable.md) il cui valore **szKey** è 040704b0, il tedesco/Unicode.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**Stringtable**](stringtable.md)
</dt> <dt>

[**VISUAL \_ STUDIO FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

[**StringFileInfo**](stringfileinfo.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni sulla versione](version-information.md)
</dt> </dl>

 

 





