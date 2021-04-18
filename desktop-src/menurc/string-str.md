---
title: Struttura di stringhe
description: Rappresenta l'organizzazione dei dati in una risorsa di versione del file. Contiene una stringa che descrive un aspetto specifico di un file, ad esempio la versione di un file, le notifiche sul copyright o i relativi marchi.
ms.assetid: fcc5ac68-4aec-4a3b-aa92-96fc50cc4ca2
keywords:
- Menu struttura stringa e altre risorse
topic_type:
- apiref
api_name:
- String
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7035223082a9e446caebd6e07d3d55c84536d09f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301193"
---
# <a name="string-structure"></a>Struttura di stringhe

Rappresenta l'organizzazione dei dati in una risorsa di versione del file. Contiene una stringa che descrive un aspetto specifico di un file, ad esempio la versione di un file, le notifiche sul copyright o i relativi marchi.

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

Tipo: **Word**

</dd> <dd>

Lunghezza, in byte, della struttura di **stringa** .

</dd> <dt>

**wValueLength**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Dimensione, in parole, del membro del **valore** .

</dd> <dt>

**wType**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Tipo di dati nella risorsa della versione. Questo membro è 1 se la risorsa della versione contiene dati di testo e 0 se la risorsa della versione contiene dati binari.

</dd> <dt>

**szKey**
</dt> <dd>

Tipo: **WCHAR**

</dd> <dd>

Stringa Unicode arbitraria. Il membro **szKey** può essere costituito da uno o più dei valori seguenti. Questi valori sono solo linee guida.

<dt>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>**Commenti**


</dt> <dd>

Il membro **value** contiene informazioni aggiuntive da visualizzare per scopi diagnostici. Questa stringa può essere di lunghezza arbitraria.

</dd> <dt>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>**CompanyName**


</dt> <dd>

Il membro **value** identifica la società che ha generato il file. Ad esempio, "Microsoft Corporation" o "Standard Microsystems Corporation, Inc."

</dd> <dt>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>**FileDescription**


</dt> <dd>

Il membro del **valore** descrive il file in modo che possa essere presentato agli utenti. Questa stringa può essere visualizzata in una casella di riepilogo quando l'utente sceglie i file da installare. Ad esempio, "driver tastiera per le tastiere in stile" o "Microsoft Word per Windows".

</dd> <dt>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>**FileVersion**


</dt> <dd>

Il membro del **valore** identifica la versione del file. Ad esempio, il **valore** potrebbe essere "3.00 a" o "5.00. RC2".

</dd> <dt>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>**InternalName**


</dt> <dd>

Il membro **value** identifica il nome interno del file, se disponibile. Ad esempio, questa stringa può contenere il nome del modulo per una DLL, un nome di dispositivo virtuale per un dispositivo virtuale Windows o un nome dispositivo per un driver di dispositivo MS-DOS.

</dd> <dt>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>**LegalCopyright**


</dt> <dd>

Il membro del **valore** descrive tutte le comunicazioni di copyright, i marchi e i marchi registrati applicabili al file. Deve includere il testo completo di tutte le comunicazioni, i simboli legali, le date di copyright, i numeri dei marchi e così via. In inglese, questa stringa deve avere il formato "Copyright Microsoft Corp. 1990 1994".

</dd> <dt>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>**LegalTrademarks**


</dt> <dd>

Il membro **valore** descrive tutti i marchi e i marchi registrati che si applicano al file. Deve includere il testo completo di tutte le comunicazioni, i simboli legali, i numeri dei marchi e così via. In inglese questa stringa dovrebbe essere "Windows is a trademark of Microsoft Corporation".

</dd> <dt>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>**OriginalFilename**


</dt> <dd>

Il membro del **valore** identifica il nome originale del file, escluso il percorso. Questo consente a un'applicazione di determinare se un file è stato rinominato da un utente. Questo nome non può essere in formato MS-DOS 8,3 Se il file è specifico di un file system non FAT.

</dd> <dt>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>**PrivateBuild**


</dt> <dd>

Il membro del **valore** descrive chi, dove e perché è stata compilata la versione privata del file. Questa stringa deve essere presente solo se il **flag \_ \_ PRIVATEBUILD di vs FF** è impostato nel membro **dwFileFlags** della struttura [**vs \_ informazione FixedFileInfo**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) . Ad esempio, il **valore** potrebbe essere "compilato da Oscar in \\ OSCAR2".

</dd> <dt>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>**ProductName**


</dt> <dd>

Il membro **valore** identifica il nome del prodotto con cui viene distribuito questo file. Questa stringa, ad esempio, potrebbe essere "Microsoft Windows".

</dd> <dt>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>**ProductVersion**


</dt> <dd>

Il membro **valore** identifica la versione del prodotto con cui viene distribuito questo file. Ad esempio, il **valore** potrebbe essere "3.00 a" o "5.00. RC2".

</dd> <dt>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>**SpecialBuild**


</dt> <dd>

Il membro del **valore** descrive il modo in cui la versione del file è diversa dalla versione normale. Questa voce deve essere presente solo se il **flag \_ \_ SPECIALBUILD di vs FF** è impostato nel membro **dwFileFlags** della struttura [**vs \_ informazione FixedFileInfo**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) . Ad esempio, il **valore** potrebbe essere "compilazione privata per Olivetti risoluzione dei problemi del mouse nei computer M250 e M250E".

</dd> </dl> </dd> <dt>

**Riempimento**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Il numero di parole necessarie per allineare il membro del **valore** a un limite di 32 bit è pari a zero.

</dd> <dt>

**Valore**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Stringa con terminazione zero. Per ulteriori informazioni, vedere la descrizione del membro **szKey** .

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura non è una vera struttura del linguaggio C perché contiene membri a lunghezza variabile. Questa struttura è stata creata esclusivamente per rappresentare l'organizzazione dei dati in una risorsa di versione e non viene visualizzata in alcun file di intestazione fornito con Windows Software Development Kit (SDK).

Una struttura di **stringa** può avere un valore **szKey** , ad esempio "CompanyName" e un **valore** "Microsoft Corporation". Un'altra struttura di **stringa** con lo stesso valore **szKey** potrebbe contenere un **valore** di "Microsoft GmbH". Questo problema può verificarsi se la seconda struttura di **stringhe** è stata associata a una struttura [**un'STRINGTABLE**](stringtable.md) il cui valore **szKey** è 040704b0, tedesco/Unicode.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**Un'STRINGTABLE**](stringtable.md)
</dt> <dt>

[**VS \_ informazione FixedFileInfo**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

[**StringFileInfo**](stringfileinfo.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni sulla versione](version-information.md)
</dt> </dl>

 

 





