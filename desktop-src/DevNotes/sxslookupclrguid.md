---
description: Recupera il nome della classe e altre informazioni associate a un GUID specificato nel manifesto di un componente.
ms.assetid: af7c6e56-604d-4a1b-8fbf-71a372ba1ae7
title: Funzione SxsLookupClrGuid
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SxsLookupClrGuid
api_type:
- DllExport
api_location:
- Mscoree.dll
- Sxs.dll
ms.openlocfilehash: 6a23a9b761cca176e91650fab7c301a05c8e7435b2d46c97b1cdf1c1c5bc2027
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103631"
---
# <a name="sxslookupclrguid-function"></a>Funzione SxsLookupClrGuid

Recupera il nome della classe e altre informazioni associate a un GUID specificato nel manifesto di un componente. Questa funzione viene usata solo quando si implementa l'interoperabilità non gestita gestita di basso livello nel .NET Framework. Per altre informazioni sull'interoperabilità non gestita, vedere "Interoperabilità con codice non gestito" in .NET Framework SDK e Applicazioni isolate e assembly [side-by-side.](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)

## <a name="syntax"></a>Sintassi


```C++
BOOL SxsLookupClrGuid(
  _In_        DWORD   dwFlags,
  _In_        LPGUID  pClsid,
  _In_opt_    HANDLE  hActCtx,
  _Inout_opt_ PVOID   pvOutputBuffer,
  _In_        SIZE_T  cbOutputBuffer,
  _Out_       PSIZE_T pcbOutputBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Combinazione di zero o più dei flag seguenti.



| Valore                                                                                                                                                                                                                                                                                             | Significato                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SXS_LOOKUP_CLR_GUID_USE_ACTCTX"></span><span id="sxs_lookup_clr_guid_use_actctx"></span><dl> <dt>**SXS \_ LOOKUP \_ CLR GUID USE \_ \_ \_ ACTCTX**</dt> <dt>0x00000001</dt> </dl>              | Se questo flag è impostato, il *parametro hActCtx* deve contenere un handle del contesto di attivazione restituito [**dalla funzione CreateActCtx.**](/windows/win32/api/winbase/nf-winbase-createactctxa) Se questo flag non è impostato, il parametro *hActCtx* viene ignorato e **SxsLookupClrGuid** cerca nel contesto di attivazione attualmente attivo (la funzione [**ActivateActCtx**](/windows/win32/api/winbase/nf-winbase-activateactctx) viene usata per rendere attivo un contesto di attivazione).<br/> |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_SURROGATE"></span><span id="sxs_lookup_clr_guid_find_surrogate"></span><dl> <dt>**SXS \_ LOOKUP \_ CLR GUID FIND \_ \_ \_ SURROGATE**</dt> <dt>0x00010000</dt> </dl>  | Se questo flag è impostato, **SxsLookupClrGuid** cerca un surrogato.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS"></span><span id="sxs_lookup_clr_guid_find_clr_class"></span><dl> <dt>**SXS \_ LOOKUP \_ CLR GUID FIND CLR \_ \_ \_ \_ CLASS**</dt> <dt>0x00020000</dt> </dl> | Se questo flag è impostato, **SxsLookupClrGuid** cerca una classe.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_ANY"></span><span id="sxs_lookup_clr_guid_find_any"></span><dl> <dt>**SXS \_ LOOKUP \_ CLR GUID FIND \_ \_ \_ ANY**</dt> <dt>0x00030000</dt> </dl>                    | Si tratta di una combinazione di **SXS \_ LOOKUP CLR GUID FIND \_ \_ \_ \_ SURROGATE** e **SXS \_ LOOKUP CLR GUID FIND CLR \_ \_ \_ \_ \_ CLASS** flag; se entrambi sono impostati, **SxsLookupClrGuid** cerca prima un surrogato e solo se non ne trova uno, quindi cerca una classe.<br/>                                                                                                                                                |



 

</dd> <dt>

*pClsid* \[ Pollici\]
</dt> <dd>

Puntatore al GUID su cui cercare le informazioni di interoperatività nel contesto di attivazione. Questo parametro non può essere **NULL.**

</dd> <dt>

*hActCtx* \[ in, facoltativo\]
</dt> <dd>

Se il flag **\_ SXS LOOKUP CLR GUID USE \_ \_ \_ \_ ACTCTX** è impostato nel parametro *dwFlags,* *hActCtx* deve contenere un handle del contesto di attivazione restituito dalla funzione [**CreateActCtx.**](/windows/win32/api/winbase/nf-winbase-createactctxa) In caso contrario, *hActCtx* viene ignorato.

</dd> <dt>

*pvOutputBuffer* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore al buffer in cui vengono copiate le informazioni restituite. Questo parametro può avere valore NULL solo se il *parametro cbOutputBuffer* ha valore zero. I dati inseriti in questo buffer all'uscita (se presenti) sono costituiti da una struttura **CLR SXS \_ GUID \_ INFORMATION \_** seguita da eventuali dati stringa aggiuntivi necessari. Per altre informazioni, vedere la sezione Osservazioni riportata di seguito.

</dd> <dt>

*cbOutputBuffer* \[ Pollici\]
</dt> <dd>

Dimensione in byte del buffer a cui punta *il parametro pvOutputBuffer.*

</dd> <dt>

*pcbOutputBuffer* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile in cui le dimensioni, in byte, delle informazioni restituite vengono inserite all'uscita. Se il *parametro cbOutputBuffer* è zero o se le dimensioni del buffer di output sono inferiori a quelle delle informazioni restituite, **SxsLookupClrGuid** ha esito negativo e [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un errore **ERROR INSUFFICIENT \_ \_ BUFFER**. In questo caso, usare il valore nella variabile a cui punta *pcbOutputBuffer* per allocare un buffer sufficientemente grande e quindi chiamare di nuovo **SxsLookupClrGuid** per recuperare le informazioni desiderate.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario. Per altre informazioni sugli errori, chiamare [ **GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

I componenti gestiti possono dichiararsi come "assembly di interoperabilità" gestiti in modo da consentire a un consumer di componenti Win32 non gestiti di fare riferimento all'assembly dichiarante. Il consumer del componente può interagire con il componente gestito chiamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) su un GUID. Il livello di interoperatività instrada la richiesta di creazione dell'oggetto .NET Framework, crea un'istanza dell'oggetto gestito e restituisce un puntatore a interfaccia.

**SxsLookupClrGuid** consente ai framework di recuperare le informazioni associate a un DETERMINATO GUID nel manifesto del componente, ad esempio il nome della classe .NET, la versione del .NET Framework richiesta e l'assembly host in cui si trova. I componenti gestiti pubblicano un assembly di interoperabilità che contiene diverse istruzioni che associano GUID ai nomi di assembly e tipi e il runtime .NET brokera la costruzione di istanze di oggetti gestiti quando viene chiamato [**CoCreateInstance.**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)

Di seguito è riportato un manifesto del componente di esempio che dichiara un GUID CLR e un surrogato CLR che può essere ricercato da **SxsLookupClrGuid:**

``` syntax
<assembly manifestVersion="1.0" xmlns=
    "urn:schemas-microsoft-com:asm.v1">
   <assemblyIdentity type="interop" name=
    "DotNet.Sample.Surrogates" version="1.0.0.0"/>
   <clrClass name="MySampleClass" clsid=
    "{19f7f420-4cc5-4b0d-8a82-c24645c0ba1f}"
      progId="MySampleClass.1" runtimeVersion="1.0.3055"/>
   <clrSurrogate name="MySampleSurrogate" clsid=
    "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}"
      runtimeVersion="1.0.3055"/>
</assembly>
```

Un provider di interoperatività chiama **SxsLookupClrGuid** con un puntatore al GUID "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}", e riceveranno come risultato il nome della classe "MySampleSurrogate", la versione di runtime richiesta "1.0.3055" e l'identità testuale "DotNet.Sample.Surrogates,version='1.0.0.0',type='interop'" del componente host.

Queste informazioni restituite sono contenute e/o a cui fa riferimento una **struttura \_ \_ \_ CLR SXS GUID INFORMATION** dichiarata come segue.

``` syntax
typedef struct _SXS_GUID_INFORMATION_CLR
{
  DWORD   cbSize;
  DWORD   dwFlags;
  PCWSTR  pcwszRuntimeVersion;
  PCWSTR  pcwszTypeName;
  PCWSTR  pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;
```

I membri di questa struttura contengono le informazioni seguenti.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Membro</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="cbSize"></span><span id="cbsize"></span><span id="CBSIZE"></span><strong>cbSize</strong><br/></td>
<td>Contiene le dimensioni della struttura SXS_GUID_INFORMATION_CLR (in questo modo la struttura può aumentare nelle versioni successive).<br/></td>
</tr>
<tr class="even">
<td><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span><strong>Dwflags</strong><br/></td>
<td>Contiene uno dei due valori di flag seguenti: <br/>
<ul>
<li>SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE (0x00000001): indica che il GUID specificato è stato associato a un &quot; surrogato.&quot;</li>
<li>SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS (0x00000002): indica che il GUID specificato è stato associato a una &quot; classe.&quot;</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="pcwszRuntimeVersion"></span><span id="pcwszruntimeversion"></span><span id="PCWSZRUNTIMEVERSION"></span><strong>pcwszRuntimeVersion</strong><br/></td>
<td>Punta a una stringa di caratteri wide con terminazione zero che identifica la versione del runtime specificata nel manifesto host per questa classe.<br/></td>
</tr>
<tr class="even">
<td><span id="pcwszTypeName"></span><span id="pcwsztypename"></span><span id="PCWSZTYPENAME"></span><strong>pcwszTypeName</strong><br/></td>
<td>Punta a una stringa di caratteri wide con terminazione zero contenente il nome della classe .NET associata al GUID specificato.<br/></td>
</tr>
<tr class="odd">
<td><span id="pcwszAssemblyIdentity"></span><span id="pcwszassemblyidentity"></span><span id="PCWSZASSEMBLYIDENTITY"></span><strong>pcwszAssemblyIdentity</strong><br/></td>
<td>Punta a una stringa di caratteri wide con terminazione zero che contiene l'identità testuale dell'assembly che ospita questa classe. Per altre informazioni sull'identità testuale, vedere Specifying Fully Qualified Type Names (Specifica di nomi di tipi completi) in Discovering Type Information at Run Time (Individuazione delle informazioni sui tipi in fase di esecuzione) &quot; in Programming with the .NET Framework in the .NET Framework &quot; &quot; &quot; &quot; &quot; SDK(Programmazione con il .NET Framework SDK).<br/></td>
</tr>
</tbody>
</table>



 

Un'applicazione non gestita può usare le informazioni restituite in questo modo per caricare la versione corretta del .NET Framework, caricare l'assembly identificato dall'elemento **pcwszAssemblyIdentity** e quindi creare un'istanza della classe denominata dall'elemento **pcwszTypeName.**

## <a name="examples"></a>Esempio

Usare il collegamento dinamico come indicato di seguito per chiamare **la funzione SxsLookupClrGuid:**


```C++
#include <windows.h>

// Declare a type for a SxsLookupClrGuid function pointer:
typedef BOOL (WINAPI* PFN_SXS_LOOKUP_CLR_GUID)
    ( IN DWORD      dwFlags,
    IN LPGUID     pClsid,
    IN HANDLE     hActCtx,
    IN OUT PVOID  pvOutputBuffer,
    IN SIZE_T     cbOutputBuffer,
    OUT PSIZE_T   pcbOutputBuffer );

// Declare an actual function pointer
PFN_SXS_LOOKUP_CLR_GUID pfn_SxsLookupClrGuid;

// Declare a handle for the system DLL
HINSTANCE hSxsDll;

// Other declarations:
BOOL isOK;
GUID exampleGuid = 
{0xFDB46CA5, 0x9477, 0x4528, 0xB4, 0xB2, 
    0x7F, 0x00, 0xA2, 0x54, 0xCD, 0xEA};
#define  OUTPUT_BUFFER_SIZE  512
unsigned char outputBuffer[OUTPUT_BUFFER_SIZE];
SIZE_T neededBufferSize;
DWORD errorCode;

#define SXS_LOOKUP_CLR_GUID_USE_ACTCTX       (0x00000001)
#define SXS_LOOKUP_CLR_GUID_FIND_SURROGATE   (0x00010000)
#define SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS   (0x00020000)
#define SXS_LOOKUP_CLR_GUID_FIND_ANY         (0x00030000) 
    // (SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS | 
    //    SXS_LOOKUP_CLR_GUID_FIND_SURROGATE)

#define SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE  (0x00000001)
#define SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS      (0x00000002)

typedef struct _SXS_GUID_INFORMATION_CLR
{
    DWORD       cbSize;
    DWORD       dwFlags;
    PCWSTR      pcwszRuntimeVersion;
    PCWSTR      pcwszTypeName;
    PCWSTR      pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;

void main()
{
// Use LoadLibrary to obtain a handle to the "SXS.DLL" system library
  hSxsDll = LoadLibrary( "sxs" );

// If SXS.DLL has loaded properly, 
// try to obtain a pointer to SxsLookupClrGuid
  if( hSxsDll != NULL )
  {
    pfn_SxsLookupClrGuid = (PFN_SXS_LOOKUP_CLR_GUID) GetProcAddress(
                            hSxsDll, "SxsLookupClrGuid" );
    if( pfn_SxsLookupClrGuid == NULL )
    {
       // (Handle failure to find SxsLookupClrGuid here...)
    }
    else
    {
      isOK = (pfn_SxsLookupClrGuid)(
                 SXS_LOOKUP_CLR_GUID_FIND_ANY,     // dwFlags
                 &exampleGuid,                     // pClsid
                 NULL,                             // hActCtx
                 (PVOID) outputBuffer,             // pvOutputBuffer
                 (SIZE_T) OUTPUT_BUFFER_SIZE,      // cbOutputBuffer
                 &neededBufferSize );              // pcbOutputBuffer
      if( isOK == FALSE )
      {
        errorCode = GetLastError( );
        if( errorCode == ERROR_INSUFFICIENT_BUFFER )
        {
          // If the allocation fails because the buffer was too small,
          // allocate a larger output buffer, of the size 
          // now indicated by "neededBufferSize", and try again.
        }
        else
        {
          // Handle other errors here
        }
      }
      else
      {
        // (Use the information here...)
      }
    }
    // Free the library instance when you're done
    FreeLibrary( hSxsDll );
  }
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Mscoree.dll; </dt> <dt>Sxs.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Applicazioni isolate e assembly affiancati](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)
</dt> <dt>

[**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa)
</dt> <dt>

[**ActivateActCtx**](/windows/win32/api/winbase/nf-winbase-activateactctx)
</dt> <dt>

[**Cocreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
