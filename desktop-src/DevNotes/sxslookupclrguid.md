---
description: Recupera il nome della classe e altre informazioni associate a un GUID specificato nel manifesto di un componente.
ms.assetid: af7c6e56-604d-4a1b-8fbf-71a372ba1ae7
title: SxsLookupClrGuid (funzione)
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
ms.openlocfilehash: 893fe6c51d0b31a6db3f34a60cac01f90297d26b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326205"
---
# <a name="sxslookupclrguid-function"></a>SxsLookupClrGuid (funzione)

Recupera il nome della classe e altre informazioni associate a un GUID specificato nel manifesto di un componente. Questa funzione viene utilizzata solo quando si implementa l'interoperabilità non gestita di basso livello nel .NET Framework. Per ulteriori informazioni sull'interoperabilità non gestita gestita, vedere l'argomento relativo all'interoperabilità con codice non gestito in .NET Framework SDK, nonché [le applicazioni isolate e gli assembly affiancati](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).

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

*dwFlags* \[ in\]
</dt> <dd>

Combinazione di zero o più dei flag seguenti.



| Valore                                                                                                                                                                                                                                                                                             | Significato                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SXS_LOOKUP_CLR_GUID_USE_ACTCTX"></span><span id="sxs_lookup_clr_guid_use_actctx"></span><dl> <dt>**SxS \_ Il \_ GUID CLR di ricerca \_ \_ Usa \_ ACTCTX**</dt> <dt>0x00000001</dt> </dl>              | Se questo flag è impostato, il parametro *hActCtx* deve contenere un handle del contesto di attivazione restituito dalla funzione [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) . Se questo flag non è impostato, il parametro *hActCtx* viene ignorato e **SxsLookupClrGuid** Cerca il contesto di attivazione attualmente attivo (la funzione [**ActivateActCtx**](/windows/win32/api/winbase/nf-winbase-activateactctx) viene utilizzata per rendere attivo un contesto di attivazione).<br/> |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_SURROGATE"></span><span id="sxs_lookup_clr_guid_find_surrogate"></span><dl> <dt>**SxS \_ RICERCA \_ del \_ GUID CLR \_ trova 0x00010000 \_ surrogato**</dt> <dt></dt> </dl>  | Se questo flag è impostato, **SxsLookupClrGuid** Cerca un surrogato.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS"></span><span id="sxs_lookup_clr_guid_find_clr_class"></span><dl> <dt>**SxS \_ RICERCA \_ CLR \_ GUID \_ trova \_ \_ classe CLR**</dt> <dt>0x00020000</dt> </dl> | Se questo flag è impostato, **SxsLookupClrGuid** cerca una classe.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_ANY"></span><span id="sxs_lookup_clr_guid_find_any"></span><dl> <dt>**SxS \_ Il \_ GUID CLR di ricerca \_ \_ trova \_ qualsiasi**</dt> <dt>0x00030000</dt> </dl>                    | Si tratta di una combinazione del **\_ GUID CLR di ricerca SxS \_ \_ \_ Find \_ surrogate** e **SxS \_ Lookup \_ CLR \_ GUID trova flag di \_ \_ \_ classe CLR** ; se sono impostati entrambi, **SxsLookupClrGuid** Cerca un surrogato per primo e solo se non ne trova uno, quindi cerca una classe.<br/>                                                                                                                                                |



 

</dd> <dt>

*pClsid* \[ in\]
</dt> <dd>

Puntatore al GUID su cui cercare le informazioni di interoperatività nel contesto di attivazione. Questo parametro non può essere **null**.

</dd> <dt>

*hActCtx* \[ in, facoltativo\]
</dt> <dd>

Se il **\_ GUID CLR di ricerca SxS usa il flag \_ \_ \_ \_ ACTCTX** è impostato nel parametro *dwFlags* , *hActCtx* deve contenere un handle del contesto di attivazione restituito dalla funzione [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) . In caso contrario, *hActCtx* viene ignorato.

</dd> <dt>

*pvOutputBuffer* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore al buffer in cui vengono copiate le informazioni di restituzione. Questo parametro può avere un valore NULL solo se il parametro *cbOutputBuffer* è con valore zero. I dati inseriti in questo buffer all'uscita (se presente) sono costituiti da una struttura **\_ \_ \_ CLR di informazioni GUID di SxS** seguita da eventuali dati stringa aggiuntivi necessari. Per ulteriori informazioni, vedere la sezione Osservazioni riportata di seguito.

</dd> <dt>

*cbOutputBuffer* \[ in\]
</dt> <dd>

Dimensioni in byte del buffer a cui punta il parametro *pvOutputBuffer* .

</dd> <dt>

*pcbOutputBuffer* \[ out\]
</dt> <dd>

Puntatore a una variabile in cui la dimensione, in byte, delle informazioni restituite viene posizionata all'uscita. Se il parametro *cbOutputBuffer* è zero o se la dimensione del buffer di output è inferiore alla dimensione delle informazioni restituite, **SxsLookupClrGuid** ha esito negativo e [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un errore di **\_ \_ buffer insufficiente**. In questo caso, usare il valore nella variabile a cui punta *pcbOutputBuffer* per allocare un buffer sufficientemente grande, quindi chiamare di nuovo **SxsLookupClrGuid** per recuperare le informazioni desiderate.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario. Per ulteriori informazioni sull'errore, chiamare [ **GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

I componenti gestiti possono dichiarare se stessi come supporto per gli assembly di interoperabilità gestiti, in modo da consentire a un consumer di componenti Win32 non gestito di fare riferimento all'assembly dichiarante. Il consumer di componenti può interagire con il componente gestito chiamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) su un GUID. Il livello di interoperabilità instrada la richiesta di creazione dell'oggetto a .NET Framework, crea un'istanza dell'oggetto gestito e restituisce un puntatore a interfaccia.

**SxsLookupClrGuid** consente ai Framework di recuperare le informazioni associate a un determinato GUID nel manifesto del componente, ad esempio il nome della classe .NET, la versione del .NET Framework richiesta e l'assembly host in cui si trova. I componenti gestiti pubblicano un assembly di interoperabilità contenente una serie di istruzioni che associano GUID a nomi di assembly e di tipi e i broker del runtime .NET la costruzione di istanze di oggetti gestiti quando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) viene chiamato.

Di seguito è riportato un esempio di manifesto del componente che dichiara un GUID CLR e un surrogato CLR che **SxsLookupClrGuid** può cercare:

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

Un provider di interoperabilità chiamerebbe **SxsLookupClrGuid** con un puntatore al GUID "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}" e riceverebbe in restituirà il nome della classe "MySampleSurrogate", la versione di runtime richiesta "1.0.3055" e l'identità testuale "DotNet. Sample. Surrogates, version =' 1.0.0.0', Type =' Interop '" del componente host.

Queste informazioni restituite sono contenute e/o a cui fa riferimento una struttura **\_ \_ \_ CLR di informazioni GUID di SxS** dichiarate come indicato di seguito.

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
<td>Contiene le dimensioni della struttura di SXS_GUID_INFORMATION_CLR (ciò consente di aumentare la struttura nelle versioni successive).<br/></td>
</tr>
<tr class="even">
<td><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span><strong>dwFlags</strong><br/></td>
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
<td>Punta a una stringa di caratteri wide con terminazione zero che contiene il nome della classe .NET associata al GUID specificato.<br/></td>
</tr>
<tr class="odd">
<td><span id="pcwszAssemblyIdentity"></span><span id="pcwszassemblyidentity"></span><span id="PCWSZASSEMBLYIDENTITY"></span><strong>pcwszAssemblyIdentity</strong><br/></td>
<td>Punta a una stringa di caratteri wide con terminazione zero che contiene l'identità testuale dell'assembly che ospita questa classe. Per ulteriori informazioni sull'identità testuale, vedere &quot; specifica dei nomi di tipo completi in &quot; &quot; individuazione delle informazioni sul tipo in fase di esecuzione in &quot; &quot; programmazione con il .NET Framework &quot; in .NET Framework SDK.<br/></td>
</tr>
</tbody>
</table>



 

Un'applicazione non gestita può utilizzare le informazioni restituite in questo modo per caricare la versione corretta del .NET Framework, caricare l'assembly identificato dall'elemento **pcwszAssemblyIdentity** , quindi creare un'istanza della classe denominata dall'elemento **pcwszTypeName** .

## <a name="examples"></a>Esempio

Utilizzare il collegamento dinamico come indicato di seguito per chiamare la funzione **SxsLookupClrGuid** :


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

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
