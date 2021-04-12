---
title: Gestione degli errori (Windows Internet)
description: La funzione GetLastError Recupera l'ultimo codice di errore per tutte le funzioni WinINet.
ms.assetid: ee619803-b2a3-4a99-a3e6-120e147843f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc175c80fd8bd10b6a3807376e1a207d805aee65
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104225192"
---
# <a name="handling-errors-windows-internet"></a><span data-ttu-id="12fab-103">Gestione degli errori (Windows Internet)</span><span class="sxs-lookup"><span data-stu-id="12fab-103">Handling Errors (Windows Internet)</span></span>

<span data-ttu-id="12fab-104">La funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) recupera l'ultimo codice di errore per tutte le funzioni WinInet.</span><span class="sxs-lookup"><span data-stu-id="12fab-104">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function retrieves the last error code for all of the WinINet functions.</span></span> <span data-ttu-id="12fab-105">Se viene restituito un errore di errore [**\_ Internet \_ esteso \_**](wininet-errors.md) , è presente una stringa o un buffer contenente un messaggio di errore dettagliato.</span><span class="sxs-lookup"><span data-stu-id="12fab-105">If [**ERROR\_INTERNET\_EXTENDED\_ERROR**](wininet-errors.md) is returned, there is a string or buffer that contains a detailed error message.</span></span> <span data-ttu-id="12fab-106">Chiamare la funzione [**InternetGetLastResponseInfo**](/windows/desktop/api/Wininet/nf-wininet-internetgetlastresponseinfoa) per recuperare il testo dell'errore esteso.</span><span class="sxs-lookup"><span data-stu-id="12fab-106">Call the [**InternetGetLastResponseInfo**](/windows/desktop/api/Wininet/nf-wininet-internetgetlastresponseinfoa) function to retrieve the extended error text.</span></span>

<span data-ttu-id="12fab-107">Per ottenere il testo dell'errore per un errore, chiamare la funzione [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) , passandogli un handle **hmodule** a Wininet.dll, che è possibile ottenere utilizzando la funzione [GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) .</span><span class="sxs-lookup"><span data-stu-id="12fab-107">To get the error text for an error, call the [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function, passing it an **HMODULE** handle to Wininet.dll, which can be obtained using the [GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) function.</span></span>

<span data-ttu-id="12fab-108">Di seguito è riportato un esempio di una funzione di gestione degli errori.</span><span class="sxs-lookup"><span data-stu-id="12fab-108">The following is an example of an error-handling function.</span></span>


```C++
#include <windows.h>
#include "strsafe.h"
#include "wininet.h"
#include <stdlib.h>
#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  INET_ERR_OUT_MSG_BOX_BUFFER_SIZE      512
#define  INET_ERR_OUT_FORMAT_BUFFER_SIZE       256

#ifdef  _UNICODE
#define _itot _itow_s
#else
#define _itot _itoa_s
#endif

// Forward declaration of helper function
void WINAPI addLastErrorToMsg( LPTSTR szMsgBuffer, DWORD dwSize );

// Function for displaying Internet Error information in a message box
BOOL WINAPI InternetErrorOut(
                              HWND hWnd,
                              DWORD dwError,
                              LPCTSTR szFailingFunctionName )
{
  HANDLE hProcHeap;
  TCHAR  szMsgBoxBuffer[INET_ERR_OUT_MSG_BOX_BUFFER_SIZE],
         szFormatBuffer[INET_ERR_OUT_FORMAT_BUFFER_SIZE],
         szConnectiveText[]  = { TEXT( "\nAdditional Information: " )},
        *szExtErrMsg         = NULL,
        *szCombinedErrMsg    = NULL;
  DWORD  dwInetError,
         dwBaseLength,
         dwExtLength = 0;

  if( ( hProcHeap = GetProcessHeap( ) ) == NULL )
  {
    StringCchCopy( szMsgBoxBuffer, INET_ERR_OUT_MSG_BOX_BUFFER_SIZE, 
      TEXT( "Call to GetProcessHeap( ) failed..." ) ); 
    goto InetErrorOutError_1;
  }

  dwBaseLength = FormatMessage(
    FORMAT_MESSAGE_FROM_HMODULE,             // dwFlags
    GetModuleHandle( TEXT("wininet.dll") ),  // lpSource
    dwError,                                 // dwMessageId
    0,                                       // dwLanguageId
    (LPTSTR)szFormatBuffer,                  // lpBuffer
    INET_ERR_OUT_FORMAT_BUFFER_SIZE,         // nSize
    NULL );                                  // * arguments

  if( !dwBaseLength )
  {
    StringCchCopy( szMsgBoxBuffer, INET_ERR_OUT_MSG_BOX_BUFFER_SIZE, 
                   TEXT( "Call to FormatMessage( ) failed..." ) ); 
    addLastErrorToMsg( szMsgBoxBuffer, 
                       INET_ERR_OUT_MSG_BOX_BUFFER_SIZE );
    goto InetErrorOutError_1;
  }

  if( FAILED( StringCchPrintf( szMsgBoxBuffer, 
                INET_ERR_OUT_MSG_BOX_BUFFER_SIZE,
                TEXT( "%s error; code: %d\nDescription: %s\n" ),
                szFailingFunctionName, dwError, szFormatBuffer ) ) )
  {
    StringCchCopy( szMsgBoxBuffer, INET_ERR_OUT_MSG_BOX_BUFFER_SIZE, 
      TEXT( "Call to StringCchPrintf( ) failed...\n" ) ); 
    goto InetErrorOutError_1;
  }

  StringCchLength( szMsgBoxBuffer, INET_ERR_OUT_MSG_BOX_BUFFER_SIZE,
                (size_t*) &dwBaseLength );
  // Adjust base-length value to count the number of bytes:
  dwBaseLength *= sizeof( TCHAR );

  if( dwError == ERROR_INTERNET_EXTENDED_ERROR )
  {
    InternetGetLastResponseInfo( &dwInetError, NULL, &dwExtLength );
    // Adjust the extended-length value to a byte count 
    // that includes the terminating null:
    ++dwExtLength *= sizeof( TCHAR );
    if( ( szExtErrMsg = (TCHAR*)HeapAlloc( hProcHeap, 0, dwExtLength)) 
         == NULL )
    {
      StringCchCat( szMsgBoxBuffer, INET_ERR_OUT_MSG_BOX_BUFFER_SIZE, 
        TEXT("\nFailure: Could not allocate buffer for addional details.")); 
      addLastErrorToMsg( szMsgBoxBuffer, 
                         INET_ERR_OUT_MSG_BOX_BUFFER_SIZE );
      goto InetErrorOutError_1;
    }

    if( !InternetGetLastResponseInfo( &dwInetError, 
                                      szExtErrMsg, 
                                      &dwExtLength ) )
    {
      StringCchCat( szMsgBoxBuffer, INET_ERR_OUT_MSG_BOX_BUFFER_SIZE, 
        TEXT( "\nCall to InternetGetLastResponseInfo( ) failed--" ) ); 
      addLastErrorToMsg( szMsgBoxBuffer, 
                         INET_ERR_OUT_MSG_BOX_BUFFER_SIZE );
      goto InetErrorOutError_2;
    }
    dwBaseLength += dwExtLength + sizeof( szConnectiveText );
  }

  if( ( szCombinedErrMsg = (TCHAR*)HeapAlloc( hProcHeap, 0, 
                                              dwBaseLength + sizeof(TCHAR) ) ) 
                         == NULL )
  {
    StringCchCat( szMsgBoxBuffer, INET_ERR_OUT_MSG_BOX_BUFFER_SIZE, 
      TEXT( "\nFailure: Could not allocate final output buffer." ) ); 
    addLastErrorToMsg( szMsgBoxBuffer, 
                       INET_ERR_OUT_MSG_BOX_BUFFER_SIZE );
    goto InetErrorOutError_2;
  }

  if( FAILED( StringCchCopy( szCombinedErrMsg, 
                dwBaseLength, szMsgBoxBuffer ) ) ||
      ( dwExtLength && 
        ( FAILED( StringCchCat( szCombinedErrMsg, 
                    dwBaseLength, szConnectiveText ) ) ||
          FAILED( StringCchCat( szCombinedErrMsg, 
                    dwBaseLength, szExtErrMsg ) ) ) ) )
  {
    StringCchCat( szMsgBoxBuffer, INET_ERR_OUT_MSG_BOX_BUFFER_SIZE, 
      TEXT( "\nFailure: Could not assemble final message." ) ); 
    goto InetErrorOutError_3;
  }

  MessageBox( hWnd, 
    szCombinedErrMsg, 
    TEXT( "Internet Error Message" ),
    MB_OK | MB_ICONERROR );
  HeapFree( hProcHeap, 0, szExtErrMsg );
  HeapFree( hProcHeap, 0, szCombinedErrMsg );

  return( TRUE );

InetErrorOutError_3:
  HeapFree( hProcHeap, 0, szCombinedErrMsg );
InetErrorOutError_2:
  HeapFree( hProcHeap, 0, szExtErrMsg );
InetErrorOutError_1:
  MessageBox( hWnd,
    (LPCTSTR) szMsgBoxBuffer,
    TEXT( "InternetErrorOut( ) Failed" ),
    MB_OK | MB_ICONERROR );
  return( FALSE );
}


void WINAPI addLastErrorToMsg( LPTSTR szMsgBuffer, DWORD dwSize )
{
  TCHAR szNumberBuffer[32];

  _itot( GetLastError( ), szNumberBuffer, 10 );
  StringCchCat( szMsgBuffer, dwSize, 
        TEXT( "\n   System Error number: " ) ); 
  StringCchCat( szMsgBuffer, dwSize, szNumberBuffer );
  StringCchCat( szMsgBuffer, dwSize, TEXT( ".\n" ) ); 
}
```



> [!Note]  
> <span data-ttu-id="12fab-109">WinINet non supporta le implementazioni del server.</span><span class="sxs-lookup"><span data-stu-id="12fab-109">WinINet does not support server implementations.</span></span> <span data-ttu-id="12fab-110">Inoltre, non deve essere utilizzato da un servizio.</span><span class="sxs-lookup"><span data-stu-id="12fab-110">In addition, it should not be used from a service.</span></span> <span data-ttu-id="12fab-111">Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="12fab-111">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 
